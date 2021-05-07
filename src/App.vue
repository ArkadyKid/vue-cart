<template>
  <div id="app" class="app">
    <header class="app__header">
      <cart-preview></cart-preview>
    </header>
    <main>
      <div class="app__cart">
        <div class="app__cart-wrapper">
          <cart-title class="app__cart-title"></cart-title>
          <ul class="app__cart-list">
            <cart-item class="app__cart-item"
                  v-for="(item, index) in items"
                  :key="index"
                  :title="item.title"
                  :description="item.description"
                  :article="item.article"
                  :count="item.count"
                  :alt="item.alt"
                  :additional="item.additional"
                  :src="require('./assets/items/' + item.src + '.jpg')"
                  :price="item.price">
            </cart-item>
          </ul>
          <install-check></install-check>
        </div>
        <cart-summary></cart-summary>
      </div>
      <viewed-products></viewed-products>
    </main>
  </div>
</template>

<script>
import CartPreview from "@/components/cart-preview";
import CartTitle from "@/components/cart-title";
import CartItem from "@/components/cart-item";
import InstallCheck from "@/components/install-check";
import CartSummary from "@/components/cart-summary";
import ViewedProducts from "@/components/viewed-products";

export default {
  name: 'App',
  components: {
    InstallCheck,
    CartPreview,
    CartTitle,
    CartItem,
    CartSummary,
    ViewedProducts,
  },
  data: () => ({
    items: [
      {
        title: 'Вытяжное устройство G2H',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-1',
        alt: 'Вытяжное устройство G2H',
        count: 1,
        price: '12 644',
      },
      {
        title: 'Вытяжное устройство BXC',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-2',
        alt: 'Вытяжное устройство BXC',
        count: 2,
        price: '25 288',
        additional: '12 644',
      },
      {
        title: 'Вытяжное устройство GHN',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item-3',
        alt: 'Вытяжное устройство GHN',
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
  padding-bottom: 116px;
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
  margin-bottom: 95px;
}

.app__cart-title {
  margin-bottom: 40px;
}

.app__cart-list {
  margin: 0;
  margin-left: 20px;
  margin-bottom: 40px;
  padding: 0;
  list-style: none;
}

.app__cart-item {
  margin-top: 20px;
}

.app__cart-item:not(:last-child) {
  padding-bottom: 20px;
  border-bottom: 1px solid var(--grey-lighter);
}
</style>
