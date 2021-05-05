<template>
  <div class="cart-title">
    <h1 class="cart-title__title">Ваша корзина</h1>
    <span class="cart-title__count">4 товара</span>
    <button class="cart-title__clear"
            type="button">Очистить корзину</button>
  </div>
</template>

<script>
export default {
  name: "cart-title",
}
</script>

<style scoped lang="css">
  .cart-title {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: baseline;
  }

  .cart-title__title {
    margin: 0;
    margin-right: 22px;
    font-size: 44px;
    font-weight: 700;
    line-height: 1.205;
  }

  .cart-title__count {
    color: var(--grey);
    font-size: 18px;
    line-height: 1.45;
  }

  .cart-title__clear {
    border: none;
    background-color: transparent;
    text-decoration: underline;
    color: var(--grey);
    font-size: 14px;
    line-height: 1.5;
    cursor: pointer;
  }

  .cart-title__clear:hover {
    text-decoration: none;
  }
</style>
