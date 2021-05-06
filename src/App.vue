<template>
  <div id="app" class="app">
    <header class="app__header">
      <cart-preview></cart-preview>
    </header>
    <main>
      <div class="app__cart">
        <div class="app__cart-wrapper">
          <cart-title class="app__cart-title"></cart-title>
          <ul class="app__item-list">
            <cart-item class="app__item"
                  v-for="(item, index) in items"
                  :key="index"
                  :title="item.title"
                  :description="item.description"
                  :article="item.article"
                  :count="item.count"
                  :additional="item.additional"
                  :src="require('./assets/items/' + item.src + '.jpg')"
                  :price="item.price">
            </cart-item>
          </ul>
          <install-check></install-check>
        </div>
        <div class="app__cart-summary">

        </div>
      </div>
    </main>
  </div>
</template>

<script>
import CartPreview from "@/components/cart-preview";
import CartTitle from "@/components/cart-title";
import CartItem from "@/components/cart-item";
import InstallCheck from "@/components/install-check";

export default {
  name: 'App',
  components: {
    InstallCheck,
    CartPreview,
    CartTitle,
    CartItem,
  },
  data: () => ({
    items: [
      {
        title: 'Вытяжное устройство G2H',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-1',
        count: 1,
        price: '12 644',
      },
      {
        title: 'Вытяжное устройство BXC',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-2',
        count: 2,
        price: '25 288',
        additional: '12 644',
      },
      {
        title: 'Вытяжное устройство GHN',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-3',
        count: 1,
        price: '12 644',
      },
    ]
  }),
}
</script>

<style scoped lang="css">
.app {
  margin: 0 auto;
  width: 1280px;
}

.app__header {
  height: 95px;
  margin-top: 64px;
  margin-bottom: 112px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.app__cart {
  display: grid;
  grid-gap: 50px;
  grid-template-columns: 2fr 1fr;
  align-items: center;
  margin-bottom: 96px;
}

.app__cart-title {
  margin-bottom: 40px;
}

.app__item-list {
  margin: 0;
  margin-left: 20px;
  margin-bottom: 40px;
  padding: 0;
  list-style: none;
}

.app__item {
  margin-top: 20px;
}

.app__item:not(:last-child) {
  padding-bottom: 20px;
  border-bottom: 1px solid var(--grey-lighter);
}

.app__cart-summary {
  border-radius: 5px;
  background-color: var(--grey-light);
}
</style>
