<template>
  <div>
    <h1>Shopping Cart</h1>
    <p>Items in cart: {{ cartItemCount }}</p>
    <button @click="addToCart({ name: 'Product 1', price: 100 })">Add Product 1</button>
  </div>
</template>

<script>
export default {
  computed: {
    cartItemCount() {
      return this.$store.getters.cartItemCount;
    }
  },
  methods: {
    addToCart(product) {
      this.$store.dispatch('addToCart', product);
    }
  }
}
</script>