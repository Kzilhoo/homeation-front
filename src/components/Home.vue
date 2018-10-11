<template>
    <div>
        <p>Bienvenue sur votre gestionnaire domotique mdr</p>
        <div v-for="product in products" :key=product.id>
            <product-component :product="product" />
        </div>
    </div>
</template>
<script>
import ProductComponent from './Product.vue'
export default {
  data () {
    return {
      products: [{id: 1, nom: 'Lampe', status: 'Allumé', image: '/static/lampe.jpeg'}, {id: 2, nom: 'Cafetière', status: 'Eteint', image: '/static/pingu.jpeg'}]
    }
  },
  components: {ProductComponent}
}
</script>
<style scoped>
</style>
