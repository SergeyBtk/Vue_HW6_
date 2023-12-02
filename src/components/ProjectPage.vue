<template>
    <div class="center">
        <HeaderComp/>
        <section class="banner center">
    <div class="banner__intro">
      <h1 class="banner__intro-title">Our Project</h1>
      <p class="banner__intro-text">Home / Project</p>
    </div>
  </section>
        <div class="project__categories">
    <div class="project__categories-wrap">
      <div :class="{ active: categories.activCategories }" class="project__categories-button"
        v-for="categories in categoriesList" :key="categories.id" @click="isActive(categories)">{{
          categories.nameCategories }}</div>
    </div>
  </div>
  <div class="project__items">
    <div class="project__item" v-for="project in projects" :key="project.id">
      <img class="project__item-img" :src="require('../assets/images/' + project.img)" alt="project.img">
      <div class="project__item-wrap">
        <div class="project__item-wrap-text">
          <h2 class="project__item-title">{{ project.title }}</h2>
          <p class="project__item-text">{{ project.text }}</p>
        </div>
        <a href="#">
          <svg xmlns="http://www.w3.org/2000/svg" width="70" height="70" viewBox="0 0 70 70" fill="none">
            <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
            <path d="M32 44L40 35L32 26" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </a>
      </div>
    </div>
  </div>
  <section class="project center">
    <div class="project__count-page">
      <div class="project__count-page-wrap">
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">01</p>
        </a>
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">02</p>
        </a>
        <a href="#" class="project__count-page-number">
          <p class="project__count-page-number-text">03</p>
        </a>
        <a href="#">
          <svg class="project__count-page-svg" xmlns="http://www.w3.org/2000/svg" width="53" height="52"
            viewBox="0 0 53 52" fill="none">
            <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
            <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </a>
      </div>
    </div>
  </section>
        <FooterComp/>
    </div>
</template>

<script>
import HeaderComp from '@/components/HeaderComp.vue'
import FooterComp from '@/components/FooterComp.vue'
export default {
    name: 'ProjectPage',
    props: ['contentsArticles'],
    components: {
        HeaderComp,
        FooterComp

    },
    
    data() {
        return {
            projects: [],
            projectBedroom: [
             {
               id: 1,
                title: "Let’s Get Solution for Building Construction Work",
                img: "image_bedroom1.jpg",
                tag: "Kitchen"
             },
             {
               id: 2,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "image_bedroom2.jpg",
                tag: "Bedroom"
             },
             {
               id: 3,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_bedroom3.jpg",
                tag: "Building"
             },
             {
               id: 4,
                title: "Design sprints are great",
                img: "image_bedroom4.jpg",
                tag: "Kitchen"
             },
          ],
          projectKitchen: [
             {
               id: 1,
                title: "Let’s Get Solution for Building Construction Work",
                img: "article_1.jpg",
                tag: "Kitchen"
             },
             {
               id: 2,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "article_4.jpg",
                tag: "Bedroom"
             },
             {
               id: 3,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_1.jpg",
                tag: "Building"
             },
             {
               id: 4,
                title: "Design sprints are great",
                img: "article_1.jpg",
                tag: "Kitchen"
             },
          ],
          projectBathroom: [
             {
               id: 1,
                title: "Let’s Get Solution for Building Construction Work",
                img: "image_bathroom1.jpg",
                tag: "Kitchen"
             },
             {
               id: 2,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "image_bathroom2.jpg",
                tag: "Bedroom"
             },
             {
               id: 3,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_bathroom2.jpg",
                tag: "Building"
             },
             {
               id: 4,
                title: "Design sprints are great",
                img: "image_bathroom1.jpg",
                tag: "Kitchen"
             },
          ],
          projectLivingroom: [
             {
               id: 1,
                title: "Let’s Get Solution for Building Construction Work",
                img: "image_4.jpg",
                tag: "Kitchen"
             },
             {
               id: 2,
                title: "Low Cost Latest Invented Interior Designing Ideas.",
                img: "image_2.jpg",
                tag: "Bedroom"
             },
             {
               id: 3,
                title: "Best For Any Office & Business Interior Solution",
                img: "image_3.jpg",
                tag: "Building"
             },
             {
               id: 4,
                title: "Design sprints are great",
                img: "image_4.jpg",
                tag: "Kitchen"
             },
          ],
            categoriesList: [
        {
          id: 1,
          nameCategories: 'Bathroom',
          activCategories: false
        },
        {
          id: 2,
          nameCategories: 'Bed Room',
          activCategories: false
        },
        {
          id: 3,
          nameCategories: 'Kitchan',
          activCategories: false
        },
        {
          id: 4,
          nameCategories: 'Living Area',
          activCategories: false
        }
      ]
            
        };
    },

    created() {
        this.projects = this.contentsArticles
    },

    methods: {
        isActive (data) {
        this.categoriesList.forEach(element => {
        element.activCategories = false
      })
      
      this.categoriesList[data.id - 1].activCategories = true
      this.$emit('activCategories', data)
      switch (data.id) {
        case 1:
          this.projects = this.projectBathroom
          break
        case 2:
          this.projects = this.projectBedroom
          break
        case 3:
          this.projects = this.projectKitchen
          break
        case 4:
          this.projects = this.projectLivingroom
          break
      }
      return this.categoriesList[data.id - 1].activCategories;
    }
    },
};
</script>

<style lang="scss" scoped>
$familyTitle: "DM Serif Display";
$familyText: "Jost";
$font-400: 400;
$font-500: 500;
$font-600: 600;
$widthSite: 1240px;
.center {
   padding-left: calc(50% - 1240px / 2);
   padding-right: calc(50% - 1240px / 2);
}
.banner {
  background-image: url("../assets/images/project_banner.jpg");
  height: 356px;
  display: flex;
  justify-content: center;
  align-items: flex-end;

  &__intro {
    text-align: center;
    background: #fff;
    padding: 41px 78px;
    border-top-left-radius: 37px;
    border-top-right-radius: 37px;

    &-title {
      color: #292f36;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
    }

    &-text {
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }
  }
}
.project__categories {
  margin-top: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;

  &-wrap {
    border-radius: 18px;
    width: 880px;
    border: 1px solid #CDA274;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    gap: 77px;
  }

  &-button {
    cursor: pointer;
    padding: 26px 66px;
    margin-left: -66px;
    margin-right: -66px;

    color: #292F36;
    text-align: center;
    font-family: $familyText;
    font-size: 18px;
    font-style: normal;
    font-weight: $font-600;
    line-height: 125%;
    letter-spacing: 0.36px;

    &:hover {
      color: #FFF;
      border-radius: 18px;
      background: #CDA274;
    }
  }

  .active {
    color: #FFF;
    border-radius: 18px;
    background: #CDA274;
  }
}
.project__items {
  margin-top: 61px;
  margin-bottom: 61px;
  column-count: 2;
}

.project__item {
  padding-bottom: 27px;
  display: inline-block;

  &-wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
    flex-direction: row;
  }
  &-img {
    width: 585px;
  }

}
.project {
  &__count-page {
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
}

</style>