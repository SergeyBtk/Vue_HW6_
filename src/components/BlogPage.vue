<template>
    <div>
        <section class="latest-post center">
      <h2 class="latest-post__title">Latest Post</h2>
      <div class="latest-post__wrap">
         <img src="@/assets/images/latest-post-img.jpg" alt="latest-post-img" class="latest-post__img">
         <div class="latest-post__content">
            <h3 class="latest-post__content-title">Low Cost Latest Invented Interior Designing Ideas</h3>
            <p class="latest-post__content-text">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis
               dignissim maximus.posuere in.Contrary to popular belief.</p>
            <p class="latest-post__content-text">Lorem Ipsum is not simply random text. It has roots in a piece of
               classica.</p>
            <div class="latest-post__content-wrap">
               <p class="latest-post__content-data">26 December, 2022</p>
               <img src="@/assets/images/row_left_blog.svg" alt="row_left_blog">
            </div>
         </div>
      </div>
   </section>
   <section class="blog center">
      <h2 class="blog__title-left">Articles & News</h2>
      <div class="blog__items">

         <div v-for="article in articles" :key="article.id">
            <!-- <div v-for="(article, index) in articles" v-if="index < 6" class="blog__item"> -->

            <div class="blog__item-image">
               <img :src="require('../assets/images/' + article.image)" :alt="article.image">
               <!-- <img :src="'@/assets/images/' + article.image" :alt="article.image"> -->

               <p class="blog__img-text">{{article.imgText}}</p>
            </div>
            <h2 class="blog__item-title">{{article.itemTitle}}</h2>
            <div class="blog__wrap-text">
               <p class="blog__item-text">{{article.itemData}}</p>
               <a href="blog-details.html">
                  <svg xmlns="http://www.w3.org/2000/svg" width="53" height="53" viewBox="0 0 53 53" fill="none">
                     <circle cx="26.5" cy="26.267" r="26" fill="#F4F0EC" />
                     <path d="M24.271 32.9525L30.2139 26.2668L24.271 19.5811" stroke="#292F36" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round" />
                  </svg>
               </a>
            </div>
         </div>

      </div>
      <div class="count__page">
         <div class="count__page-wrap">
            <a href="#" class="count__page-number">
               <p class="count__page-number-text">01</p>
            </a>
            <a href="#" class="count__page-number">
               <p class="count__page-number-text">02</p>
            </a>
            <a href="#" class="count__page-number">
               <p class="count__page-number-text">03</p>
            </a>
            <a href="#">
               <svg class="count__page-svg" xmlns="http://www.w3.org/2000/svg" width="53" height="52"
                  viewBox="0 0 53 52" fill="none">
                  <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
                  <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2"
                     stroke-linecap="round" stroke-linejoin="round" />
               </svg>
            </a>
         </div>
      </div>
   </section>
    </div>
</template>

<script>
export default {
    name: 'HW5ProyectBlogPage',

    data() {
        return {
            articles: [
          {
            id: 0,
             image: "blog_image_1.jpg",
             imgText: "Kitchan Design",
             itemTitle: "Let’s Get Solution For Building Construction Work",
             itemData: "26 December,2022"
          },
          {
            id: 1,
             image: "blog_image_2.jpg",
             imgText: "Living Design",
             itemTitle: "Low Cost Latest Invented Interior Designing Ideas.",
             itemData: "22 December,2022"
          },
          {
            id: 2,
             image: "blog_image_3.jpg",
             imgText: "Interior Design",
             itemTitle: "Best For Any Office & Business Interior Solution",
             itemData: "25 December,2022"
          },
          {
            id: 3,
             image: "blog_image_1.jpg",
             imgText: "Kitchan Design",
             itemTitle: "Let’s Get Solution For Building Construction Work",
             itemData: "26 December,2022"
          },
          {
            id: 4,
             image: "blog_image_2.jpg",
             imgText: "Living Design",
             itemTitle: "Low Cost Latest Invented Interior Designing Ideas.",
             itemData: "22 December,2022"
          },
          {
            id: 5,
             image: "blog_image_3.jpg",
             imgText: "Interior Design",
             itemTitle: "Best For Any Office & Business Interior Solution",
             itemData: "25 December,2022"
          },
          {
            id: 6,
             image: "blog_image_1.jpg",
             imgText: "Kitchan Design",
             itemTitle: "Let’s Get Solution For Building Construction Work",
             itemData: "26 December,2022"
          },
          {
            id: 7,
             image: "blog_image_2.jpg",
             imgText: "Living Design",
             itemTitle: "Low Cost Latest Invented Interior Designing Ideas.",
             itemData: "22 December,2022"
          },
          {
            id: 8,
             image: "blog_image_3.jpg",
             imgText: "Interior Design",
             itemTitle: "Best For Any Office & Business Interior Solution",
             itemData: "25 December,2022"
          },
       ]
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>
    $familyTitle: "DM Serif Display";
    $familyText: "Jost";
    $font-400: 400;
    $font-500: 500;
    $widthSite: 1240px;
.blog {
   margin-top: 96px;
   margin-bottom: 96px;
   &__title {
      margin-bottom: 12px;
      color: #292f36;
      text-align: center;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 1px;
      &-left {
         text-align: left;
         margin-top: 150px;
         margin-bottom: 30px;
         color: #292f36;
         font-family: $familyTitle;
         font-size: 50px;
         font-style: normal;
         font-weight: $font-400;
         line-height: 125%;
         letter-spacing: 1px;
      }
   }
   &__text {
      padding-left: calc(($widthSite - 811px) / 2);
      padding-right: calc(($widthSite - 811px) / 2);
      margin-bottom: 52px;
      color: #4d5053;
      text-align: center;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
   }
   &__items {
      display: grid;
      grid-template-columns: repeat(3, 382px);
      gap: 27px;
   }
   &__item {
      border: 1px solid #e7e7e7;
      border-radius: 62px;
      padding: 21px;
      &-select {
         background: #f4f0ec;
      }
   }
   &__item-image {
      position: relative;
      & img {
         border-top-left-radius: 62px;
         border-top-right-radius: 62px;
         margin-bottom: 21px;
      }
      & p {
         position: absolute;
         top: 228px;
         left: 20px;
         border-radius: 8px 8px 8px 0px;
         background: #fff;
         padding: 4px 10px 8px 11px;
         color: #4d5053;
         font-family: $familyText;
         font-size: 16px;
         font-style: normal;
         font-weight: $font-400;
         line-height: 150%;
         letter-spacing: 0.16px;
         text-transform: capitalize;
      }
   }
   &__item-title {
      margin-bottom: 30px;
      color: #292f36;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 0.5px;
   }
   &__wrap-text {
      display: flex;
      flex-wrap: nowrap;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
   }
   &__item-text {
      color: #4d5053;
      font-family: $familyText;
      font-size: 16px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.16px;
      text-transform: capitalize;
   }
}
.latest-post {
   &__title {
      margin-top: 200px;
      margin-bottom: 27px;
      color: #292f36;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: 400;
      line-height: 125%; /* 62.5px */
      letter-spacing: 1px;
   }
   &__wrap {
      border: 1px solid #e7e7e7;
      display: flex;
      gap: 62px;
      padding: 22px;
      border-radius: 62px;
      align-items: center;
   }
   &__img {
      border-radius: 50px;
   }
   &__content {
      width: 489px;
      &-title {
         margin-bottom: 22px;
         color: #292f36;
         font-family: $familyTitle;
         font-size: 25px;
         font-style: normal;
         font-weight: $font-400;
         line-height: 125%;
         letter-spacing: 0.5px;
      }
      &-text {
         margin-bottom: 41px;
         color: #4d5053;
         font-family: $familyText;
         font-size: 22px;
         font-style: normal;
         font-weight: $font-400;
         line-height: 150%;
         letter-spacing: 0.22px;
      }
      &-wrap {
         display: flex;
         justify-content: space-between;
         align-items: center;
         flex-wrap: nowrap;
      }
      &-data {
         color: #4d5053;
         font-family: $familyText;
         font-size: 16px;
         font-style: normal;
         font-weight: $font-400;
         line-height: 150%;
         letter-spacing: 0.16px;
         text-transform: capitalize;
      }
   }
}

.count__page {
   margin-top: 51px;
   margin-bottom: 200px;
   display: flex;
   justify-content: center;
   &-wrap {
      display: flex;
      gap: 20px;
   }
   &-number {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: nowrap;
      border: 1px #cda274 solid;
      width: 52px;
      height: 52px;
      border-radius: 52px;
      &-text {
         color: #292f36;
         font-family: $familyText;
         font-size: 16px;
         font-style: normal;
         font-weight: $font-500;
         line-height: 150%;
         text-transform: capitalize;
      }
      &:hover {
         background: #f4f0ec;
         border: none;
         width: 54px;
         height: 54px;
      }
   }
   &-svg:hover {
      fill: #f4f0ec;
      & circle {
         stroke: none;
      }
   }
}
</style>