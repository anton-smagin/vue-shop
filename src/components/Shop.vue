<template>
  <div class="row">
    <div class="items col7">
      <div v-for="(item, index) in items" v-bind:key="index" class="col3">
        <img :src="item.img" height="100" width="auto">
        <p>{{ item.name }}</p>
        <button v-on:click="addItem(item)" class="add-item btn">+</button>
      </div>
    </div>
    <div class="cart col3">
      <div v-for="(item, index) in cart" v-bind:key="index" class="cart-item">
        <img :src="item.img" height="50" width="auto">
        <p>{{ item.name }}</p>
      </div>
      <template v-if="cart.length > 0">
        <button v-on:click="clearCart" class="clear-cart row btn btn-danger">
          Clear cart
        </button>
        <button v-on:click="clearCart" class="checkout-cart row btn btn">
          Checkout
        </button>
      </template>
    </div>
  </div>
</template>


<script>
export default {
  data: function () {
    return {
      items: [
        { img: '/pokeball.png', name: 'Pokebol' },
        { img: '/light_saber.jpeg', name: 'Light Saber' },
      ],
      cart: []
    }
  },
  methods: {
    addItem: function(item) {
      this.cart.push(item)
    },
    clearCart: function() {
      this.cart = []
    }
  }
}
</script>

<style>
.row {
  clear: both;
  width: 100%;
}

.col7 {
  width: 66.6%;
  float: left;
}

.col3 {
  width: 33.3%;
  float: left;
}

.btn {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

.btn-danger {
  background-color: #f44336;
}
</style>
