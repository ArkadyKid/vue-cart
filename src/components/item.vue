<template>
  <li class="item">
    <img class="item__img"
         :src="'../assets/items/' + src + '.jpg'"
         alt="продукт"
         width="100" height="100">
    <div class="item__info">
      <h5 class="item__title">{{ title }}</h5>
      <p class="item__description">{{ description }}</p>
      <span class="item__article">{{ article }}</span>
    </div>
    <div class="item__counter">
      <button class="item__counter-button">-</button>
      <span class="item__counter-count">{{ count }}</span>
      <button class="item__counter-button">+</button>
    </div>
    <span class="item__price">{{ price }} &#8381;</span>
    <button class="item__del" type="button">
      <svg width="12" height="12"
           class="item__del-icon">
        <use xlink:href="../assets/sprite.svg#cross"></use>
      </svg>
    </button>
  </li>
</template>

<script>
export default {
  name: "item",
  props: {
    src: {
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
    article: {
      type: String,
      default: '',
    },
    count: {
      type: Number,
      default: 0,
    },
    price: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="css">
  .item {
    position: relative;
    display: grid;
    grid-template-columns: 130px minmax(auto, 343px) 1fr 1fr;
    align-items: center;
  }

  .item__img {
    margin-right: 30px;
  }

  .item__del {
    position: absolute;
    top: 0;
    right: 0;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }

  .item__del-icon {
    stroke: var(--black);
  }

  .item__info {
    margin-right: 80px;
  }

  .item__title {
    margin: 0;
    margin-bottom: 6px;
    font-weight: 600;
    line-height: 1.45;
  }

  .item__description {
    margin: 0;
    margin-bottom: 7px;
    color: var(--black-light);
    font-size: 12px;
    line-height: 1.5;
  }

  .item__article {
    font-size: 14px;
    line-height: 1.5;
    color: var(--grey);
  }

  .item__counter {
    display: grid;
    grid-gap: 2px;
    grid-template-columns: repeat(3, 34px);
    justify-content: center;
  }

  .item__counter-button,
  .item__counter-count {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 34px;
    width: 34px;
    background-color: var(--grey-light);
    border: none;
  }

  .item__counter-button {
    cursor: pointer;
  }

  .item__counter-button:first-of-type {
    border-radius: 4px 0 0 4px;
  }

  .item__counter-button:last-of-type {
    border-radius: 0 4px 4px 0;
  }

  .item__price {
    text-align: center;
  }
</style>
