<template>
    <div>
        <h1>
            Your Cart:
        </h1>
        <ShoppingCart :items="this.$root.$data.cart">

        </ShoppingCart>
    </div>

</template>


<script>
    import ShoppingCart from '../components/ShoppingCart.vue'
    export default {
        name: 'Cart',
        components: {
            ShoppingCart
        },
    }
</script>

<style scoped>
    div{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>