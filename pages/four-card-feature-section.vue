<template>
  <div class="page">
    <div class="container">
      <span class="subtitle">Reliable, efficient delivery</span>
      <h1 class="heading">Powered by Technology</h1>
      <p
        class="text"
      >Our Artifical Intelligence powered tools use millions of project data points to ensure that your project is successful</p>

      <div class="grid">
        <div class="grid_item cyan">
          <h3 class="grid_item_heading">Supervisor</h3>
          <p class="grid_item_text">Monitors activity to identify project roadblocks</p>
          <img
            src="/four-card-feature-section/icon-supervisor.svg"
            class="grid_item_icon"
            alt="Supervisor"
          />
        </div>
        <div class="grid_item red">
          <h3 class="grid_item_heading">Team Builder</h3>
          <p class="grid_item_text">Scans our talent network to creat optimal team for your project</p>
          <img
            src="/four-card-feature-section/icon-team-builder.svg"
            class="grid_item_icon"
            alt="Supervisor"
          />
        </div>
        <div class="grid_item orange">
          <h3 class="grid_item_heading">Karma</h3>
          <p class="grid_item_text">Regularly evaluates our talent to ensuire quality</p>
          <img
            src="/four-card-feature-section/icon-karma.svg"
            class="grid_item_icon"
            alt="Supervisor"
          />
        </div>
        <div class="grid_item blue">
          <h3 class="grid_item_heading">Calculator</h3>
          <p
            class="grid_item_text"
          >Uses data from past projects to provide better delivery estimates</p>
          <img
            src="/four-card-feature-section/icon-calculator.svg"
            class="grid_item_icon"
            alt="Supervisor"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;600&display=swap');

$primary-red: hsl(0, 78%, 62%);
$primary-cyan: hsl(180, 62%, 55%);
$primary-orange: hsl(34, 97%, 64%);
$primary-blue: hsl(212, 86%, 64%);

$neutral-dark-blue: hsl(234, 12%, 34%);
$neutral-grey-blue: hsl(229, 6%, 66%);
$neutral-light-grey: hsl(0, 0%, 98%);

$body-font: 15px;

.page {
  font-family: 'Poppins', -apple-system, Arial, sans-serif;
  font-size: $body-font;
  background-color: #fafafa;
  padding: 90px 32px;
  min-height: 100vh;
  text-align: center;
}

.container {
  max-width: 1110px;
  margin: 0 auto;
}

.subtitle {
  font-size: 1.9em;
  font-weight: 200;
  margin-bottom: 25px;
  color: $neutral-dark-blue;
}

.heading {
  font-size: 1.9em;
  font-weight: 600;
  color: $neutral-dark-blue;
}

.text {
  margin: 24px auto 0;
  max-width: 500px;
  color: $neutral-grey-blue;
}

.grid {
  margin-top: 66px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-auto-flow: column;
  align-items: center;
  grid-gap: 24px;
}

.grid_item {
  border-radius: 6px;
  background-color: #fff;
  border-top: 4px solid transparent;
  text-align: left;
  padding: 24px;
  box-shadow: 0 5px 15px 0 rgba($neutral-dark-blue, 0.2);

  .grid_item_heading {
    font-weight: 600;
    margin-bottom: 8px;
    color: $neutral-dark-blue;
  }

  .grid_item_text {
    max-width: 90%;
    font-size: 0.8em;
    color: $neutral-grey-blue;
    line-height: 1.8;
  }

  .grid_item_icon {
    margin-top: 24px;
    margin-left: auto;
    margin-right: 0;
    display: block;
  }

  &.cyan {
    grid-row: span 2;
    border-top-color: $primary-cyan;
  }

  &.red {
    border-top-color: $primary-red;
  }

  &.orange {
    border-top-color: $primary-orange;
  }

  &.blue {
    grid-row: span 2;
    border-top-color: $primary-blue;
  }
}

@media (max-width: 636px) {
  .subtitle,
  .heading {
    font-size: 1.6em;
  }

  .grid {
    grid-template-columns: 100%;
    grid-template-rows: auto;
    grid-auto-flow: row;
  }

  .grid_item {
    &.cyan,
    &.blue {
      grid-row: auto;
    }
  }
}
</style>
