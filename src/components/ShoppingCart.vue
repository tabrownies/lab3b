<template>
    <ul v-if="items.length > 0">
        <li class="cart-item" v-for="(item, index) in items" :key="item.id">
            <img :src="'/images/products/'+item.image">
            <h2>
                {{item.name}}
            </h2>
            <p>
                Price: {{item.price}}
            </p>
            <button class="auto" @click="removeFromCart(index)">Remove</button>
        </li>
    </ul>
    <h3 v-else>
        There are no items in your cart
    </h3>

</template>


<script>
    export default {
        name: 'ShoppingCart',
        props: {
            items: Array
        },
        methods: {
            removeFromCart(index) {
                console.log(this.$root.$data.cart.splice(index, 1));
            }
        }
    }
</script>

<style scoped>
    .cart-item {
        width: 100%;
        margin: 12px;
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
        box-sizing: border-box;
        list-style: none;
        border: 3px solid #F2921D;
        border-radius: 3px
    }


    .cart-item img,
    .cart-item h2,
    .cart-item p {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0px 15px;
    }

    .cart-item img {
        height: 200px;
        padding-top: 15px;
    }

    .cart-item h2 {
        font-size: 40px;
    }

    .cart-item p {
        font-size: 35px;
    }
</style>