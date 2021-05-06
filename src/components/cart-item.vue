<template>
  <li class="cart-item">
    <img class="cart-item__img"
         :src="src"
         alt="продукт"
         width="100" height="100">
    <div class="cart-item__info">
      <h5 class="cart-item__title">{{ title }}</h5>
      <p class="cart-item__description">{{ description }}</p>
      <span class="cart-item__article">{{ article }}</span>
    </div>
    <div class="cart-item__counter">
      <button class="cart-item__counter-button">-</button>
      <span class="cart-item__counter-count">{{ count }}</span>
      <button class="cart-item__counter-button">+</button>
      <span class="cart-item__counter-additional" v-if="additional">{{ additional }} &#8381;/шт.</span>
    </div>
    <span class="cart-item__price">{{ price }} &#8381;</span>
    <button class="cart-item__del" type="button">
      <svg width="12" height="12"
           class="cart-item__del-icon">
        <use xlink:href="../assets/sprite.svg#cross"></use>
      </svg>
    </button>
  </li>
</template>

<script>
export default {
  name: "cart-item",
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
    additional: {
      type: String,
      default: '',
    }
  },
}
</script>

<style scoped lang="css">
  .cart-item {
    position: relative;
    display: grid;
    grid-template-columns: 130px minmax(auto, 343px) 1fr 1fr;
    align-items: center;
  }

  .cart-item__img {
    margin-right: 30px;
  }

  .cart-item__del {
    position: absolute;
    top: 0;
    right: 0;
    padding: 0;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }

  .cart-item__del-icon {
    stroke: var(--black);
  }

  .cart-item__info {
    margin-right: 80px;
  }

  .cart-item__title {
    margin: 0;
    margin-bottom: 6px;
    font-weight: 600;
    line-height: 1.45;
  }

  .cart-item__description {
    margin: 0;
    margin-bottom: 7px;
    color: var(--black-light);
    font-size: 12px;
    line-height: 1.5;
  }

  .cart-item__article {
    font-size: 14px;
    line-height: 1.5;
    color: var(--grey);
  }

  .cart-item__counter {
    position: relative;
    display: grid;
    gap: 2px;
    grid-template-columns: repeat(3, 34px);
    justify-content: center;
  }

  .cart-item__counter-button,
  .cart-item__counter-count {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 34px;
    width: 34px;
    background-color: var(--grey-light);
    border: none;
  }

  .cart-item__counter-button {
    padding: 0;
    cursor: pointer;
  }

  .cart-item__counter-button:first-of-type {
    border-radius: 4px 0 0 4px;
  }

  .cart-item__counter-button:last-of-type {
    border-radius: 0 4px 4px 0;
  }

  .cart-item__price {
    text-align: center;
  }

  .cart-item__counter-additional {
    position: absolute;
    bottom: calc(calc(12px * -1.45) - 8px);
    left: 50%;
    transform: translateX(-50%);
    font-size: 12px;
    line-height: 1.45;
  }
</style>
