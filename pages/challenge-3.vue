<template>
  <div class="page">
    <header class="header">
      <a href="#" class="logo">
        <img src="~static/challenge-3/logo.svg" alt="Huddle" class="logo_img" />
      </a>
    </header>
    <div class="content">
      <img src="~static/challenge-3/illustration-mockups.svg" alt="Mockup" class="content_img" />
      <div class="content_text">
        <h1>Build The Community Your Fans Will Love</h1>
        <p>Huddle re-imagines the way we build communities. You have a voice, but so does your audience. Create connections with your users as you engage in genuine discussion.</p>
        <button class="button">Register</button>
      </div>
    </div>
    <footer class="footer">
      <a href="#" class="footer_link">
        <font-awesome-icon :icon="['fab', 'facebook-f']" class="footer_icon" />
      </a>
      <a href="#" class="footer_link">
        <font-awesome-icon :icon="['fab', 'twitter']" class="footer_icon" />
      </a>
      <a href="#" class="footer_link">
        <font-awesome-icon :icon="['fab', 'instagram']" class="footer_icon" />
      </a>
    </footer>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Huddle landing page | Amanda Ng'
    }
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&family=Poppins:wght@400;600&display=swap');

$primary-violet: hsl(257, 40%, 49%);

$body-font: 16px;

$max-width: 1280px;

.page {
  font-family: 'Open Sans', -apple-system, Arial, sans-serif;
  font-size: $body-font;
  min-height: 100vh;
  background-color: $primary-violet;
  background-image: url('~static/challenge-3/bg-desktop.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  justify-content: space-between;
  flex-direction: column;
  display: flex;
  padding: 0 60px 40px;
  margin: 0 auto;
  color: #fff;
}

.header {
  margin: 0 auto;
  max-width: $max-width;
  padding: 50px 0;
  width: 100%;
}

.logo {
  width: 200px;
  display: block;
}

.logo_img {
  width: 100%;
}

.content {
  margin: 0 auto;
  max-width: $max-width;
  grid-gap: 60px;
  display: grid;
  align-items: center;
  grid-template-columns: 1fr 41%;
  width: 100%;
}

.content_img {
  width: 100%;
}

.content_text h1 {
  font-family: 'Poppins', -apple-system, Arial, sans-serif;
  font-size: 2.2em;
  margin-bottom: 30px;
}

.content_text p {
  font-size: 1.2em;
}

.button {
  width: 200px;
  height: 60px;
  text-align: center;
  border-radius: 50px;
  color: $primary-violet;
  font-size: 1.1em;
  margin-top: 30px;
  box-shadow: 0 4px 10px 0px rgba(0, 0, 0, 0.5);
  transition: transform 0.3s, box-shadow 0.3s;
  outline: 0;

  &:hover {
    transform: translateY(-1px);
    box-shadow: 0 4px 10px 0px rgba(0, 0, 0, 0.8);
  }
}

.footer {
  margin-top: 20px;
  display: grid;
  grid-gap: 15px;
  justify-content: flex-end;
  grid-auto-flow: column;
}

.footer_link {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  border: 1px solid #fff;
  cursor: pointer;
}

.footer_icon {
  width: 100%;
  height: 100%;
  padding: 10px;
  color: #fff;
}

@media (max-width: 768px) {
  .page {
    background-image: url('~static/challenge-3/bg-mobile.svg');
    background-position: top center;
    background-size: 100%;
  }

  .content {
    display: block;
  }

  .content_img {
    display: block;
    max-width: 400px;
    margin: 0 auto;
  }

  .content_text {
    margin-top: 90px;
    text-align: center;
  }

  .button {
    width: 400px;
    max-width: 80%;
  }

  .footer {
    margin-top: 80px;
    justify-content: center;
  }
}
</style>
