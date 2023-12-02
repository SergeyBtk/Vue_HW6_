<template>
    <div>
        <h1>TEST COMPONENT</h1>
        <div v-for="item in contentsArticles" :key="item.id">
            {{ item.id }} <br>
            {{ item.title }} <br>
            {{ item.tag }} <br>
            {{ item.img }} <br>
            <!-- <img src="" alt=""> -->
            <img class="article__img" :src="require('../assets/images/' + item.img)" alt="article.img">
        </div>
    </div>
</template>

<script>
export default {
    name: 'TestNew',
    props: ['contentsArticles'],

    data() {
        return {
            
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

</style>