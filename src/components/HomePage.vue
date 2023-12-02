<template>
    <div>
        <section class="project center">
      <h2 class="project__title">Follow Our Projects</h2>
      <p class="project__text">It is a long established fact that a reader will be distracted by the of readable content
         of page lookings at its layouts points.</p>
      <div class="project__item-wrap">
         <div class="project__item">
            <img src="@/assets/images/image_1.jpg" alt="image 1" class="project__item-img-1">
            <div class="project__item-content">
               <div class="project__text-wrap">
                  <h2 class="project__item-title">Modern Kitchan</h2>
                  <p class="project__item-text">Decor / Artchitecture</p>
               </div>
               <img src="@/assets/images/row_left_item.svg" alt="">
            </div>
         </div>
         <div class="project__item">
            <img src="@/assets/images/image_2.jpg" alt="image 2" class="project__item-img-2">
            <div class="project__item-content">
               <div class="project__text-wrap">
                  <h2 class="project__item-title">Modern Kitchan</h2>
                  <p class="project__item-text">Decor / Artchitecture</p>
               </div>
               <img src="@/assets/images/row_left_item.svg" alt="">
            </div>
         </div>
         <div class="project__item">
            <img src="@/assets/images/image_3.jpg" alt="image 3" class="project__item-img-3">
            <div class="project__item-content">
               <div class="project__text-wrap">
                  <h2 class="project__item-title">Modern Kitchan</h2>
                  <p class="project__item-text">Decor / Artchitecture</p>
               </div>
               <img src="@/assets/images/row_left_item.svg" alt="">
            </div>
         </div>
         <div class="project__item">
            <img src="@/assets/images/image_4.jpg" alt="image 4" class="project__item-img-4">
            <div class="project__item-content">
               <div class="project__text-wrap">
                  <h2 class="project__item-title">Modern Kitchan</h2>
                  <p class="project__item-text">Decor / Artchitecture</p>
               </div>
               <img src="@/assets/images/row_left_item.svg" alt="">
            </div>
         </div>
      </div>
   </section>
   <section class="counter center">
      <div class="counter__wrap">
         <div class="counter__item">
            <h2 class="counter__item-title">12</h2>
            <p class="counter__item-text">Years Of Experiance</p>
         </div>
         <div class="counter__item">
            <h2 class="counter__item-title">85</h2>
            <p class="counter__item-text">Success Project</p>
         </div>
         <div class="counter__item">
            <h2 class="counter__item-title">15</h2>
            <p class="counter__item-text">Active Project</p>
         </div>
         <div class="counter__item">
            <h2 class="counter__item-title">95</h2>
            <p class="counter__item-text">Happy CUstomers</p>
         </div>
      </div>
   </section>
   <section class="blog center">
      <h2 class="blog__title">Articles & News</h2>
      <p class="blog__text">It is a long established fact that a reader will be distracted by the of readable content of
         a page when lookings at its layouts the points of using.</p>
      <div class="blog__items">

         <div class="blog__item">
            <div class="blog__item-image">
               <img src="@/assets/images/blog_image_1.jpg" alt="blog-image-1">
               <p class="blog__img-text">Kitchan Design</p>
            </div>
            <h2 class="blog__item-title">Let’s Get Solution For Building Construction Work</h2>
            <div class="blog__wrap-text">
               <p class="blog__item-text">26 December,2022</p>
               <img src="@/assets/images/row_left_blog.svg" alt="row_left_blog">
            </div>
         </div>

         <div class="blog__item blog__item-select">
            <div class="blog__item-image">
               <img src="@/assets/images/blog_image_2.jpg" alt="blog-image-2">
               <p class="blog__img-text">Living Design</p>
            </div>
            <h2 class="blog__item-title">Low Cost Latest Invented Interior Designing
               Ideas.</h2>
            <div class="blog__wrap-text">
               <p class="blog__item-text">22 December,2022</p>
               <img src="@/assets/images/row_left_blog_select.svg" alt="row_left_blog">
            </div>
         </div>

         <div class="blog__item">
            <div class="blog__item-image">
               <img src="@/assets/images/blog_image_3.jpg" alt="blog-image-3">
               <p class="blog__img-text">Interior Design</p>
            </div>
            <h2 class="blog__item-title">Best For Any Office & Business Interior
               Solution</h2>
            <div class="blog__wrap-text">
               <p class="blog__item-text">25 December,2022</p>
               <img src="@/assets/images/row_left_blog.svg" alt="row_left_blog">
            </div>
         </div>
      </div>
   </section>
    </div>
</template>

<script>
export default {
    name: 'HW5ProyectHomePage',

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
    $familyTitle: "DM Serif Display";
    $familyText: "Jost";
    $font-400: 400;
    $font-500: 500;
    $widthSite: 1240px;
.project {
   margin-top: 96px;
   margin-bottom: 96px;
   &__title {
      margin-bottom: 8px;
      color: #292f36;
      text-align: center;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 1px;
   }
   &__text {
      padding-left: calc(($widthSite - 737px) / 2);
      padding-right: calc(($widthSite - 737px) / 2);
      color: #4d5053;
      text-align: center;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
   }
   &__item-wrap {
      margin-top: 93px;
      display: grid;
      column-gap: 100px;
      row-gap: 56px;
      grid-template-columns: repeat(2, 550px);
   }
   &__item-img-1 {
      border-top-right-radius: 75px;
   }
   &__item-img-2 {
      border-top-left-radius: 75px;
   }
   &__item-img-3 {
      border-bottom-right-radius: 75px;
   }
   &__item-img-4 {
      border-bottom-left-radius: 75px;
   }
   &__item-content {
      margin-top: 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
   }
   &__item-title {
      color: #292f36;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 0.5px;
   }
   &__item-text {
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
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

.counter {
   padding-top: 151px;
   padding-bottom: 151px;
   background-color: #f4f0ec;
   &__wrap {
      padding-left: 59px;
      padding-right: 59px;
   }
   &__wrap {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
   }
   &__item {
      text-align: center;
      display: flex;
      row-gap: 16px;
      flex-direction: column;
      & {
         display: inline-block;
         border-right: 1px solid #cda274;
         padding-right: 60px;
      }
      &:last-child {
         border-right: none;
      }
   }
   &__item-title {
      color: #cda274;
      font-family: "DM Serif Display";
      font-size: 85px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 1.7px;
   }
   &__item-text {
      color: #4d5053;
      font-family: "Jost";
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
   }
}
</style>