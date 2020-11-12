<template>
  <div class="v-catalog-item">
    <img class="v-catalog-item__image" :src=" require('../assets/images/' + product_data.image) " alt="img">
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">Цена: {{ product_data.price }}</p>
    <button
      class="v-catalog-item__add_to_cart_btn btn"
      @click="SendDataToParent"
    >Добавить в корзину</button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      dafult() {
        return {}
      }
    }
  },
  methods: {
    SendDataToParent() {
      this.$emit('send-data-to-parent', this.product_data.article)
      console.log(123)
    }
  }
}
</script>

<style lang="sass">
  @import "../assets/styles/variables.sass"

  .v-catalog-item
    flex-basis: 25%
    box-shadow: 0 0 8px 0 #e0e0e0
    padding: $pd*2
    margin-bottom: $mrg*2
    &__image
      width: 100px
</style>