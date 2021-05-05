<template>
  <div class="cart-preview">
    <svg width="32" height="32" class="cart-preview__icon">
      <use xlink:href="../assets/sprite.svg#cart"></use>
    </svg>
    <div class="cart-preview__wrapper">
      <span class="cart-preview__title">Ваша корзина</span>
      <span class="cart-preview__count">3 товара</span>
      <span class="cart-preview__price">50 576 &#8381;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "app-cart",
}
</script>

<style scoped lang="css">
  .cart-preview {
    display: grid;
    grid-template-columns: auto auto;
  }

  .cart-preview__icon {
    align-self: center;
    margin-right: 10px;
    fill: var(--blue);
    stroke: var(--white);
  }

  .cart-preview__wrapper {
    display: grid;
    grid-template-rows: auto auto auto;
  }

  .cart-preview__title {
    font-size: 14px;
    line-height: 1.5;
  }

  .cart-preview__count,
  .cart-preview__price {
    font-size: 12px;
    line-height: 1.45;
  }

  .cart-preview__count {
    color: var(--grey);
  }
</style>
