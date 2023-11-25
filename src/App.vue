<template>
	<h1>{{ name }}</h1>
	<button @click="placeOrder">Place Order</button>
	<YummyMeal name="Hamburger 🍔" :price="6" @addToCart="addItemToCart" />
</template>

<script>
	import YummyMeal from './components/YummyMeal.vue';
	export default {
		components: {
			YummyMeal,
		},
		setup() {
			const name = 'The Snazzy Burger';

			function placeOrder() {
				alert('Your order has been placed');
			}
			const addItemToCart = (item) => alert(`One ${item} added to cart`);

			return { name, placeOrder, addItemToCart };
		},
	};
</script>
