<template>
  <li class="viewed-item">
    <img :src="src"
         :alt="alt"
         class="viewed-item__img"
         width="250" height="250">
    <h5 class="viewed-item__title">{{ title }}</h5>
    <p class="viewed-item__description">{{ description }}</p>
    <p class="viewed-item__price-ruble">{{ priceRubleMin }} &#8381; - {{ priceRubleMax }} &#8381;</p>
    <p class="viewed-item__price-euro">{{ priceEuroMin }} &#8364; - {{ priceEuroMax }} &#8364;</p>
    <a :href="href" class="viewed-item__link">Подробнее</a>
  </li>
</template>

<script>
export default {
  name: "viewed-item",
  props: {
    src: {
      type: String,
      default: '',
    },
    alt: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
    priceRubleMin: {
      type: String,
      default: '',
    },
    priceRubleMax: {
      type: String,
      default: '',
    },
    priceEuroMin: {
      type: String,
      default: '',
    },
    priceEuroMax: {
      type: String,
      default: '',
    },
    href: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="css">
  .viewed-item {
    display: grid;
    grid-template-rows: 245px auto 1fr auto auto;
    padding: 25px;
    max-height: 563px;
    background-color: var(--grey-light);
    border-radius: var(--border-radius-background);
  }

  .viewed-item__img {
    display: block;
    align-self: center;
    max-width: 100%;
    height: auto;
    object-fit: contain;
    margin-bottom: 5px;
  }

  .viewed-item__title {
    margin: 0;
    margin-bottom: 10px;
    font-size: 22px;
    line-height: 1.2052;
    font-weight: 700;
  }

  .viewed-item__description {
    margin: 0;
    padding: 0;
    font-size: 14px;
    line-height: 1.45;
  }

  .viewed-item__price-ruble {
    margin: 0;
    padding: 0;
    margin-bottom: 3px;
    font-size: 22px;
    line-height: 1.3;
    font-family: 'Roboto', 'Arial', sans-serif;
    font-weight: 500;
  }

  .viewed-item__price-euro {
    margin: 0;
    padding: 0;
    margin-bottom: 20px;
    color: var(--grey);
    font-size: 16px;
    line-height: 1.45;
  }

  .viewed-item__link {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-basis: 100%;
    padding: 14px;
    text-decoration: none;
    color: var(--white);
    background-color: var(--blue);
    border-radius: var(--border-radius-card);
  }

  .viewed-item__link:hover {
    opacity: 0.7;
  }
</style>
