<template>
    <ShoppingCart :items="this.$root.$data.cart">

    </ShoppingCart>
</template>


<script>
    import ShoppingCart from '../components/ShoppingCart.vue'
    export default {
        name: 'Cart',
        components:{
            ShoppingCart
        },
    }
</script>