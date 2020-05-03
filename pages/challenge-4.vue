<template>
  <div class="page">
    <div class="content-wrapper">
      <div class="content">
        <header class="header">
          <a href="#">
            <img src="~static/challenge-4/logo.svg" alt="Base Apparel" class="logo" />
          </a>
        </header>
        <img src="~static/challenge-4/hero-mobile.jpg" alt="Hero" class="hero_mobile" />
        <h1 class="heading">
          We're
          <br />
          <span class="highlight">coming soon</span>
        </h1>
        <p
          class="text"
        >Hello fellow shoppers! We're currently building our new fashion store. Add your email below to stay up-to-date with announcements and our launch deals.</p>
        <form
          class="input-box"
          v-bind:class="{'error': error}"
          type="post"
          @submit="checkForm"
          novalidate
        >
          <input
            v-model="email"
            type="email"
            name="email"
            class="input"
            placeholder="Email Address"
          />
          <img v-if="error" class="error-icon" src="~static/challenge-4/icon-error.svg" />
          <button type="submit" class="button">
            <img src="~/static/challenge-4/icon-arrow.svg" alt="Submit" class="button_img" />
          </button>
        </form>
        <span v-if="error" class="error-msg">{{ error }}</span>
      </div>
    </div>
    <div class="hero_desktop" />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Base apparel page | Amanda Ng'
    }
  },
  data: function() {
    return {
      error: null,
      email: ''
    }
  },
  methods: {
    checkForm: function(e) {
      this.error = null

      if (!this.email || this.email.trim().length === 0) {
        this.error = 'Email address is required'
      } else if (!this.validateEmail(this.email)) {
        this.error = 'Please provide a valid email address'
      }

      if (this.error) e.preventDefault()
    },
    validateEmail(email) {
      var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/

      return re.test(String(email).toLowerCase())
    }
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300;400;600&display=swap');

$primary-red: hsl(0, 36%, 70%);
$primary-soft-red: hsl(0, 93%, 68%);

$neutral-red: hsl(0, 6%, 24%);

$gradient-1: linear-gradient(135deg, hsl(0, 0%, 100%), hsl(0, 100%, 98%));
$gradient-2: linear-gradient(135deg, hsl(0, 80%, 86%), hsl(0, 74%, 74%));

$body-font: 16px;

$max-width: 1280px;

.page {
  font-family: 'Josefin Sans', -apple-system, Arial, sans-serif;
  font-size: $body-font;
  min-height: 100vh;

  display: flex;
  background: $gradient-1;
}

.content-wrapper {
  flex: 0 0 57%;
  background-size: cover;
  background-image: url('~static/challenge-4/bg-pattern-desktop.svg');

  display: flex;
  align-items: center;
}

.content {
  width: 100%;
  max-width: 445px;
  margin: 40px auto;
  padding: 0 40px;
}

.heading {
  color: $primary-red;
  text-transform: uppercase;
  font-weight: 300;
  margin-top: 135px;
  font-size: 48px;
  letter-spacing: 20px;
  line-height: 1.2;

  .highlight {
    color: $neutral-red;
    font-weight: 600;
  }
}

.text {
  margin-top: 40px;
  color: $primary-red;
  line-height: 1.5;
}

.input-box {
  margin-top: 50px;
  border: 1px solid rgba($primary-red, 0.6);
  border-radius: 25px;
  display: flex;
  margin-right: 50px;
  align-items: center;
  justify-content: space-between;
  position: relative;

  &.error {
    border-color: $primary-soft-red;
  }
}

.input {
  flex: 1 1 auto;
  border: 0;
  font-size: 16px;
  font-family: inherit;
  background: transparent;
  color: $neutral-red;
  padding: 0px 30px;
  height: 48px;
  outline: 0;
  border-top-left-radius: 25px;
  border-bottom-left-radius: 25px;

  &::placeholder {
    color: $primary-red;
    opacity: 0.6;
  }

  &:-internal-autofill-selected {
    background: transparent;
    color: $primary-red;
  }
}

.error-icon {
  width: 24px;
  height: 24px;
  margin-right: 85px;
}

.error-msg {
  display: block;
  font-size: 14px;
  margin: 8px 0 0px 30px;
  color: $primary-soft-red;
}

.button {
  border: 0;
  outline: 0;
  height: 50px;
  width: 100px;
  border-radius: 25px;
  background: linear-gradient(135deg, hsl(0, 80%, 86%) 50%, hsl(0, 74%, 74%));
  background-size: 200% 100%;
  background-position: 100% 100%;
  position: absolute;
  right: -30px;

  transition: all 0.3s;
}

.button:hover {
  background-position: 0%;
  box-shadow: 0 10px 10px 0px rgba(hsl(0, 80%, 86%), 0.4);
}

.hero_desktop {
  flex: 0 0 43%;
  background-image: url('~static/challenge-4/hero-desktop.jpg');
  background-size: cover;
  background-position: 50% 0%;
}

.hero_mobile {
  display: none;
}

@media (max-width: 768px) {
  .content-wrapper {
    flex: 1 1 auto;
  }

  .content {
    max-width: 100%;
    padding: 0;
    margin: 0;
  }

  .header {
    margin: 30px;
  }

  .logo {
    width: 100px;
  }

  .heading {
    text-align: center;
    margin: 68px 30px 25px;
  }

  .text {
    text-align: center;
    margin: 25px 30px 40px;
  }

  .input-box {
    margin: 30px;
  }

  .button {
    width: 60px;
    right: 0;
  }

  .hero_mobile {
    display: block;
    width: 100%;
  }

  .hero_desktop {
    display: none;
  }
}
</style>
