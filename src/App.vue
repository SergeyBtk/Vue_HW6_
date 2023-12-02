<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <HeaderComp/>
  <HeaderBannerComp/> -->
  <ProjectPage :contentsArticles="contentsArticles"/>
  <!-- <BlogDetailsPage/>
  <HomePage/>
  <BlogPage/>
  <FooterComp/>
  <ProductDetails/> -->
  <!-- <TestNew :contentsArticles="contentsArticles"/> -->

</template>

<script>
// import HeaderComp from './components/HeaderComp.vue'
// import HeaderBannerComp from './components/HeaderBannerComp.vue'
// import BlogDetailsPage from './components/BlogDetailsPage.vue'
// import BlogPage from './components/BlogPage.vue'
// import FooterComp from './components/FooterComp.vue'
// import ProductDetails from './components/ProductDetails.vue'
// import HomePage from './components/HomePage.vue'
import ProjectPage from './components/ProjectPage.vue'
// import TestNew from './components/TestNew.vue';

export default {
  name: 'App',
  components: {
    //  BlogDetailsPage,
    //  BlogPage,
    //  HeaderComp,
    //  HeaderBannerComp,
    //  FooterComp,
    //  ProductDetails,
    //  HomePage,
    ProjectPage,
   //  TestNew
},
   data() {
        return {
         contentsArticles: [
            {
               id: 0,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_4.jpg",
                tag: "Building"
             },
             {
               id: 1,
                title: "Let’s Get Solution for Building Construction Work",
                img: "article_1.jpg",
                tag: "Kitchen"
             },
             {
               id: 2,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "image_2.jpg",
                tag: "Bedroom"
             },
             
             {
               id: 4,
                title: "Design sprints are great",
                img: "image_bathroom1.jpg",
                tag: "Kitchen"
             },
             {
               id: 5,
                title: "Let’s Get Solution for Building Construction Work",
                img: "image_bathroom2.jpg",
                tag: "Kitchen"
             },
             {
               id: 6,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "image_1.jpg",
                tag: "Bedroom"
             },
             {
               id: 7,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_3.jpg",
                tag: "Building"
             },
             {
               id: 8,
                title: "Design sprints are great",
                img: "article_4.jpg",
                tag: "Kitchen"
             },
          ],
          buttonList: [
             "Kitchen",
             "Bedroom",
             "Building",
             "Architecture",
             "Kitchen Planning",
             "Bathroom"
          ]
            
        };
    },
}
</script>

<style lang="scss">
* {
   margin: 0;
   padding: 0;
}
.center {
   padding-left: calc(50% - 1240px / 2);
   padding-right: calc(50% - 1240px / 2);
}
a {
   text-decoration: none;
}
</style>
