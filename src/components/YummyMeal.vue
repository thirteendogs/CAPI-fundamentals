<template>
	<p>
		<strong>{{ name }}</strong>
		{{ price }}
	</p>
	<button @click="addToCart">Add to Cart</button>
</template>

<script>
	export default {
		props: {
			name: String,
			price: Number,
		},
		setup(props, { emit }) {
			const addToCart = () => emit('addToCart', props.name);
			return { addToCart };
		},
	};
</script>
