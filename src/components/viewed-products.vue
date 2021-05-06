<template>
  <div class="viewed-products">
    <div class="viewed-products__wrapper">
      <h2 class="viewed-products__title">Просмотренные товары</h2>
      <div class="viewed-products__navigation">
        <button type="button"
                class="viewed-products__navigation-button">
          <svg width="50" height="50" class="viewed-products__navigation-icon">
            <use xlink:href="../assets/sprite.svg#navigation"></use>
          </svg>
        </button>
        <p class="viewed-products__navigation-wrapper">
          <span class="viewed-products__navigation-page">1</span>
          <span class="viewed-products__navigation-separator">&nbsp;/&nbsp;</span>
          <span class="viewed-products__navigation-total">6</span>
        </p>
        <button type="button"
                class="viewed-products__navigation-button">
          <svg width="50" height="50" class="viewed-products__navigation-icon">
            <use xlink:href="../assets/sprite.svg#navigation"></use>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "viewed-products"
}
</script>

<style scoped lang="css">
  .viewed-products__title {
    margin: 0;
    font-size: 30px;
    line-height: 1.2052;
    font-weight: 600;
  }

  .viewed-products__wrapper {
    display: grid;
    grid-template-columns: auto auto;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    margin-bottom: 47px;
  }
  .viewed-products__navigation {
    display: grid;
    grid-template-columns: 50px auto 50px;
    align-items: center;
    gap: 20px;
  }

  .viewed-products__navigation-wrapper {
    margin: 0;
    padding: 0;
  }

  .viewed-products__navigation-button {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
    border: none;
    background-color: transparent;
    cursor: pointer;
  }

  .viewed-products__navigation-button:hover {
    opacity: 0.7;
  }

  .viewed-products__navigation-button:last-of-type {
    transform: scale(-1, 1);
  }

  .viewed-products__navigation-total,
  .viewed-products__navigation-separator {
    color: var(--grey);
    font-size: 18px;
    line-height: 1.5;
  }

  .viewed-products__navigation-page {
    font-size: 24px;
    line-height: 1.5;
    font-weight: 500;
  }
</style>
