<template>
  <div class="v-catalog">
    <h1>Каталог</h1>
    <div class="v-catalog__list">
      <v-catalog-item
        v-for="product in products"
        :key="product.article"
        :product_data="product"
        @send-data-to-parent="showChildArticleConsole"
      ></v-catalog-item>
    </div>
  </div>
</template>

<script>
import vCatalogItem from './v-catalog-item'

export default {
  name: "v-catalog",
  components: {
    vCatalogItem
  },
  data() {
    return {
      products: [
        {
          image: "1.jpg",
          name: "Футболка 1",
          price: 2100.234234234,
          article: "T1",
          available: true,
          category: "Мужские"
        },
        {
          image: "2.jpg",
          name: "Футболка 2",
          price: 3150.12312412,
          article: "T2",
          available: true,
          category: "Женские"
        },
        {
          image: "3.jpg",
          name: "Футболка 3",
          price: 4200.51524,
          article: "T3",
          available: false,
          category: "Женские"
        },
        {
          image: "4.jpg",
          name: "Футболка 4",
          price: 5300.1245512,
          article: "T4",
          available: true,
          category: "Мужские"
        },
        {
          image: "5.jpg",
          name: "Футболка 5",
          price: 6500.3522314,
          article: "T5",
          available: false,
          category: "Женские"
        },
        {
          image: "6.jpeg",
          name: "Футболка 6",
          price: 8700.4124123,
          article: "T6",
          available: true,
          category: "Женские"
        }
      ]
    }
  },
  methods: {
    showChildArticleConsole(data) {
      console.log(data)
    }
  }
}
</script>

<style lang="sass">
  @import "../assets/styles/variables.sass"

  .v-catalog
    &__list
      display: flex
      flex-wrap: wrap
      justify-content: space-between
      align-items: center
</style>