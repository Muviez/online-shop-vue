<template>
  <div class="v-main-wrapper">
    <v-catalog></v-catalog>
    <v-cart></v-cart>
  </div>
</template>

<script>
import vCatalog from './v-catalog'
import vCart from './v-cart'

export default {
  name: "v-main-wrapper",
  components: {
    vCatalog,
    vCart
  }
}
</script>

<style lang="sass">
  @import "../assets/styles/variables.sass"
  .v-main-wrapper
    max-width: 900px
    margin: 0 auto

</style>