<template>
    <div>
        <div v-for="product in products" :key="product.id">
            <h1> {{ product.name }}</h1>
            <h2> цена: {{ formattedPrice(product.price) }}</h2>
            

            <div v-if="product.available">
                <h2> Availeble</h2>
            </div>
            <div v-else>
                <h2> Out of stock</h2>
            </div>
            <br>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',

    data() {
        return {
            moneta: '',
            products: [
                {
                    id: 1,
                    name: 'product 1',
                    price: 1000,
                    available: true
                },
                {
                    id: 2,
                    name: 'product 2',
                    price: 500,
                    available: true
                },
                {
                    id: 3,
                    name: 'product 3',
                    price: 2000,
                    available: false
                },
                {
                    id: 4,
                    name: 'product 4',
                    price: 1300,
                    available: true
                },
            ],
        };
    },
    computed: {
        formattedPrice () {
        return price => `$ ${price}`
        },
    },
};
</script>

<style lang="scss" scoped>

</style>