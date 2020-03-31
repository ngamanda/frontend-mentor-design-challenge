<template>
  <div class="page">
    <div class="grid">
      <div class="header">
        <h1 class="heading">Join our community</h1>
        <h3 class="subtitle">30-day, hassle-free money back guarantee</h3>
        <p class="description">
          Gain access to our library of tutorials along with export code
          reviews.
          <br />Perfect for any developers who are serious about honing their skills
        </p>
      </div>
      <div class="subscription">
        <h3 class="subtitle">Monthly Subscription</h3>
        <div class="price">
          <span class="price__value">$29</span>
          <span class="price__period">per month</span>
        </div>
        <p class="price__footer">Full access for less than $1 a day</p>
        <button class="sign-up__button">Sign Up</button>
      </div>
      <div class="footer">
        <h3 class="subtitle">Why Us</h3>
        <ul class="list">
          <li>Tutorials by industry experts</li>
          <li>Peer & expert code review</li>
          <li>Coding exercises</li>
          <li>Access to our GitHub repos</li>
          <li>Community forum</li>
          <li>Flashcard decks</li>
          <li>New videos every week</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Karla:wght@400;700&display=swap');

$primary-cyan: hsl(179, 62%, 43%);
$primary-yellow: hsl(71, 73%, 54%);

$neutral-gray: hsl(204, 43%, 93%);
$neutral-blue: hsl(218, 22%, 67%);

$body-font: 16px;

.page {
  font-family: 'Karla', -apple-system, Arial, sans-serif;
  font-size: $body-font;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #e6eff6;
  min-height: 100vh;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 100%;
  max-width: 636px;
  overflow: hidden;
  border-radius: 8px;
  background-color: #fff;
  box-shadow: 0 0 20px 0px $neutral-blue;
}

.header,
.subscription,
.footer {
  padding: 40px;
}

.subtitle {
  font-size: 1.2em;
}

.header {
  grid-column: 1 / span 2;

  .heading {
    font-size: 1.4em;
    color: $primary-cyan;
    margin-bottom: 30px;
  }

  .subtitle {
    color: $primary-yellow;
  }

  .description {
    margin-top: 20px;
    line-height: 1.5;
    color: $neutral-blue;
  }
}

.subscription {
  color: #fff;
  background-color: $primary-cyan;

  .price {
    display: flex;
    align-items: center;
    margin: 20px 0 14px;

    .price__value {
      font-size: 2em;
      font-weight: 700;
    }

    .price__period {
      margin-left: 12px;
      opacity: 0.6;
    }
  }

  .price__footer {
    font-size: 0.95em;
  }

  .sign-up__button {
    font-size: 1em;
    margin-top: 30px;
    border-radius: 4px;
    background-color: $primary-yellow;
    font-weight: 700;
    padding: 14px;
    color: #fff;
    width: 100%;
    box-shadow: 0 0 5px 3px rgba(black, 0.05);
    transition: box-shadow 0.3s ease;
    outline: 0;

    &:hover {
      box-shadow: 0 0 5px 3px rgba(black, 0.2);
    }
  }
}

.footer {
  color: #fff;
  background-color: rgba($primary-cyan, 0.75);

  .list {
    margin-top: 24px;
    list-style: none;
    padding: 0;
    opacity: 0.8;
    line-height: 1.4;
  }
}

@media (max-width: 636px) {
  .page {
    display: block;
    min-height: 0;
  }

  .grid {
    border-radius: 0;
    min-height: 100vh;
    grid-template-columns: 100%;
    grid-template-rows: auto auto 1fr;
    box-shadow: none;
  }

  .header,
  .subscription,
  .footer {
    padding: 30px 24px;
  }

  .header {
    grid-column: 1;
  }
}
</style>
