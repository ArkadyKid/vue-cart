<template>
  <div id="app" class="app">
    <header class="app__header">
      <cart-preview></cart-preview>
    </header>
    <main>
      <div class="app__cart">
        <div class="app__cart-wrapper">
          <cart-title class="app__cart-title"></cart-title>
          <ul class="app__item-list"
          >
            <item class="app__item"
                  v-for="(item, index) in items"
                  :key="index"
                  :title="item.title"
                  :description="item.description"
                  :article="item.article"
                  :count="item.count"
                  :src="item.src"
                  :price="item.price"></item>
          </ul>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import CartPreview from "@/components/cart-preview";
import CartTitle from "@/components/cart-title";
import Item from "@/components/item";

export default {
  name: 'App',
  components: {
    CartPreview,
    CartTitle,
    Item,
  },
  data: () => ({
    items: [
      {
        title: 'Вытяжное устройство G2H',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item',
        count: 1,
        price: '12 644',
      },
      {
        title: 'Вытяжное устройство G2H',
        description: '12-72/168 м3/ч / гидрорегулируемый расход / от датчика присутствия',
        article: 'Артикул: G2H1065',
        src: 'item',
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
    grid-template-columns: 2fr 1fr;
  }

  .app__cart-title {
    margin-bottom: 40px;
  }

  .app__item-list {
    margin: 0;
    margin-left: 20px;
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
</style>
