<template>
  <div class="install-check">
    <input type="checkbox" class="install-check__checkbox">
    <img src="../assets/install-decoration.png"
         alt="installation"
         width="50" height="50">
    <div class="install-check__text-block">
      <h5 class="install-check__title">Установка</h5>
      <p class="install-check__description">Отметьте, если Вам необходима консультация профессионала по монтажу выбранных товаров.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "install-check",
}
</script>

<style scoped lang="css">
  .install-check {
    display: grid;
    grid-template-columns: 20px 50px 1fr;
    align-items: center;
    gap: 20px;
    padding: 28px 25px;
    border-radius: var(--border-radius-background);
    background-color: var(--grey-light);
  }

  .install-check__text-block {
    display: grid;
    grid-template-rows: auto auto;
  }

  .install-check__checkbox {
    width: 20px;
    height: 20px;
    border-color: var(--grey);
    cursor: pointer;
  }

  .install-check__title {
    margin: 0;
    margin-bottom: 2px;
    font-size: 16px;
    line-height: 1.45;
    font-weight: 600;
  }

  .install-check__description {
    margin: 0;
    font-size: 14px;
    line-height: 1.5;
    color: var(--grey);
  }
</style>
