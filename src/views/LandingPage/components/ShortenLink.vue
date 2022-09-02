<template>
  <Container>
    <div class="shorten">
      Short
      <div class="input">
        <!-- <img src="@/assets/bg-shorten-desktop.svg" alt="" class="input__img" /> -->
        <div class="text-wrap">
          <input
            type="text"
            class="input__text"
            :class="`${isError ? 'error--active' : ''}`"
            placeholder="Shorten a link here..."
            :value="currentLink"
            @input="handleChangeCurrentLink"
          />
          <div class="error-mess" :class="`${isError ? 'error--active' : ''}`">
            Please add a link
          </div>
        </div>

        <CustomeButton
          inputClass="primary minRadius"
          @click="handleShortenLink"
        >
          Shorten It!
        </CustomeButton>
      </div>
      <div class="short-list">
        <div v-for="item in shortenList" :key="item" class="short-item">
          <div class="origin-link">{{ item.origin }}</div>
          <div class="action">
            <div class="short-link">
              <div class="text">{{ item.short }}</div>
              <CustomeButton
                inputClass="primary1 minRadius"
                @click="() => handleCoppy(item.id)"
                :class="coppiedLinkId === item.id && 'active'"
              >
                {{ coppiedLinkId === item.id ? "Copied!" : "Copy" }}
              </CustomeButton>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Container>
</template>

<script>
import CustomeButton from "../../../Element/CustomeButton.vue";
import Container from "../../../layout/Container.vue";

export default {
  components: {
    CustomeButton,
    Container,
  },
  data() {
    return {
      shortenList: [
        {
          id: this.makeid(5),
          origin:
            "https://www.google.com/search?gs_ssp=eJzj4tLP1TcwKivMqjIxYHRg8OJKP7xAIaf04e6ZyQBsaglp&q=g%C3%A0+lu%E1%BB%99c&oq=g%C3%A0+nu%E1%BB%99c&aqs=chrome.1.69i57j46i10i131i433j0i10l2j0i10i457j0i10l4.3084j0j7&sourceid=chrome&ie=UTF-8",
          short: `shortly.at/${this.makeid(5)}`,
        },
      ],
      currentLink: "",
      isError: false,
      coppiedLinkId: null,
    };
  },
  methods: {
    makeid(length) {
      let result = "";
      const characters =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
      const charactersLength = characters.length;
      for (var i = 0; i < length; i++) {
        result += characters.charAt(
          Math.floor(Math.random() * charactersLength)
        );
      }
      return result;
    },
    handleCoppy(id) {
      this.coppiedLinkId = id;
    },
    handleShortenLink() {
      if (this.currentLink) {
        this.shortenList = [
          ...this.shortenList,
          {
            id: this.makeid(5),
            origin: this.currentLink,
            short: `shortly.at/${this.makeid(5)}`,
          },
        ];
        this.currentLink = "";
      } else {
        this.isError = true;
      }
    },

    handleChangeCurrentLink(e) {
      const value = e.target.value;
      this.currentLink = value;
      if (value) {
        this.isError = false;
      }
    },
  },
};
</script>

<style scoped>
.shorten {
  position: relative;
  width: 100%;
}

.input {
  padding: 50px;
  position: absolute;
  top: -100px;
  left: 0;
  right: 0;
  background-color: var(--bg-color2);
  background-image: url("@/assets/bg-shorten-desktop.svg");
  background-size: cover;

  display: flex;
  justify-content: space-between;
  column-gap: 20px;
  border-radius: 10px;
}
.text-wrap {
  flex: 1;
  padding: 0 20px;
  display: flex;
  flex-direction: column;
}
.input__text {
  border-radius: 10px;
  border: none;
  width: calc(100% - 42px);
  padding: 16px 32px;
  border: 2px solid transparent;
}

.input__text.error--active {
  border: 2px solid red;
}

.input__text.error--active::placeholder {
  color: var(--red-color);
}

.input__text:focus {
  outline: none;
}
.input__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.origin-link {
  flex: 1;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
}

.short-list {
  margin-top: 60px;
}

.short-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 32px;
  background-color: white;
  border-radius: 10px;
  box-shadow: var(--box-shadow-color) 0px 0.5rem 1rem 0px;
  column-gap: 30px;
}

.short-link {
  display: flex;
  align-items: center;
  column-gap: 30px;
}

.short-link .text {
  color: var(--primary-color1);
}

.short-item + .short-item {
  margin-top: 20px;
}

.error-mess {
  color: var(--red-color);
  display: none;
  margin-top: 10px;
  font-style: italic;
  position: absolute;
  bottom: 24px;
}

.error-mess.error--active {
  display: block;
}
</style>
