<template>
  <div class="cart-summary">
    <h5 class="cart-summary__title">Итого</h5>
    <dl class="cart-summary__list">
      <div class="cart-summary__list-wrapper">
        <dt class="cart-summary__list-term">Сумма заказа</dt>
        <dd class="cart-summary__list-definition">50 576 &#8381;</dd>
      </div>
      <div class="cart-summary__list-wrapper">
        <dt class="cart-summary__list-term">Колличество</dt>
        <dd class="cart-summary__list-definition">4 шт</dd>
      </div>
      <div class="cart-summary__list-wrapper">
        <dt class="cart-summary__list-term">Установка</dt>
        <dd class="cart-summary__list-definition">Нет</dd>
      </div>
    </dl>
    <div class="cart-summary__price">
      <hr>
      <p class="cart-summary__price-wrapper">
        <span class="cart-summary__price-text">Стоимость товаров</span>
        <span class="cart-summary__price-number">50 576 &#8381;</span>
      </p>
    </div>
    <div class="cart-summary__buttons">
      <button type="button"
              class="cart-summary__button cart-summary__button--checkout">
        Оформить заказ</button>
      <button type="button"
              class="cart-summary__button">
        Купить в 1 клик</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "cart-summary"
}
</script>

<style scoped lang="css">
  .cart-summary {
    display: grid;
    grid-template-rows: repeat(4, auto);
    gap: 30px;
    padding: 35px 30px;
    border-radius: var(--border-radius-background);
    background-color: var(--grey-light);
  }

  .cart-summary__title {
    margin: 0;
    font-size: 24px;
    font-weight: 600;
    line-height: 1.2052;
  }

  .cart-summary__list {
    display: grid;
    gap: 18px;
    grid-template-rows: repeat(3, auto);
    margin: 0;
    font-weight: 500;
    line-height: 1.45;
  }

  .cart-summary__list-wrapper {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
    font-weight: 400;
  }

  .cart-summary__list-definition {
    margin: 0;
    text-align: right;
    font-family: 'Roboto', 'Arial', sans-serif;
  }

  .cart-summary__price hr {
    border: 1px solid #AEB0B6;
    margin: 0;
    margin-bottom: 16px;
  }

  .cart-summary__price-wrapper {
    display: grid;
    gap: 10px;
    align-items: center;
    grid-template-columns: repeat(2, 1fr);
    margin: 0;
  }

  .cart-summary__price-text {
    font-size: 18px;
    line-height: 1.45;
  }

  .cart-summary__price-number {
    font-family: 'Roboto', 'Arial', sans-serif;
    font-size: 26px;
    font-weight: 700;
    line-height: 1.3;
    text-align: right;
  }

  .cart-summary__buttons {
    display: grid;
    grid-template-rows: repeat(2, auto);
    gap: 12px;
  }

  .cart-summary__button {
    border: 1px solid var(--blue);
    padding: 14px;
    border-radius: var(--border-radius-card);
    width: 100%;
    text-align: center;
    vertical-align: center;
    color: var(--blue);
    background-color: var(--white);
    cursor: pointer;
  }

  .cart-summary__button--checkout {
    background-color: var(--blue);
    color: var(--white);
  }

  .cart-summary__button:hover {
    opacity: 0.7;
  }
</style>
