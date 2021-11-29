<template>
  <div id="app">
    <!-- header  -->
    <siteHeader :navBar="navBar" />
    <!-- hero image  -->
    <heroImage />
    <!-- MAIN  -->
    <siteMain
      :corsiSlide1="corsiSlide1"
      :corsiSlide2="corsiSlide2"
      :corsiSlide3="corsiSlide3"
    />
    <!-- footer -->
    <siteFooter />
  </div>
</template>

<script>
// importazioni
import siteHeader from "./components/header.vue";
import heroImage from "./components/heroImage.vue";
import siteMain from "./components/main.vue";
import siteFooter from "./components/footer.vue";
// font
import "@fontsource/montserrat";

export default {
  name: "App",
  components: {
    siteHeader,
    heroImage,
    siteMain,
    siteFooter,
  },
  data() {
    return {
      navBar: [
        {
          name: "home",
          dd1: "link1",
          dd2: "link2",
          dd3: "link3",
        },
        {
          name: "pages",
          dd1: "link1",
          dd2: "link 2",
          dd3: "link 3",
        },
        {
          name: "courses",
          dd1: "link1",
          dd2: "link 2",
          dd3: "link 3",
        },
        {
          name: "features",
          dd1: "link1",
          dd2: "link 2",
          dd3: "link 3",
        },
        {
          name: "blog",
          dd1: "link1",
          dd2: "link 2",
          dd3: "link 3",
        },
        {
          name: "shop",
          dd1: "link1",
          dd2: "link 2",
          dd3: "link 3",
        },
      ],
      corsiSlide1: [
        {
          img: "slide.jpg",
          price: "$40.",
          free: false,
          value: "00",
          descrition: "Learning to write as a professional Author",
          lessons: "20 lessons",
          students: "50 students",
        },
        {
          img: "slide2.jpg",
          price: "$0.",
          value: "00",
          descrition: "Customer-Centric info-Tech Strategist",
          free: true,
          lessons: "24 lessons",
          students: "769 students",
        },
        {
          img: "slide3.jpg",
          price: "$19.",
          value: "00",
          free: false,
          descrition: "Open Programming Courses for Everyone: Python",
          lessons: "17 lessons",
          students: "62 students",
        },
      ],
      corsiSlide2: [
        {
          img: "https://images.pexels.com/photos/6929180/pexels-photo-6929180.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$0.",
          free: true,
          value: "00",
          descrition:
            "Corso completo di Data Science e machine learning con Python",
          lessons: "40 lessons",
          students: "10 students",
        },
        {
          img: "https://images.pexels.com/photos/6929190/pexels-photo-6929190.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$12.",
          value: "00",
          descrition: "Guida Pratica e Completa a Django, Python e Bootstrap",
          free: false,
          lessons: "5 lessons",
          students: "300 students",
        },
        {
          img: "https://images.pexels.com/photos/39284/macbook-apple-imac-computer-39284.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$30.",
          value: "00",
          free: false,
          descrition:
            "Social Media Marketing - Il Corso Completo con Certificato",
          lessons: "7 lessons",
          students: "70 students",
        },
      ],
      corsiSlide3: [
        {
          img: "https://images.pexels.com/photos/6224/hands-people-woman-working.jpg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$110.",
          free: false,
          value: "00",
          descrition: "FACEBOOK ADS GURU 2021 - Corso operativo completo",
          lessons: "10 lessons",
          students: "30 students",
        },
        {
          img: "https://images.pexels.com/photos/6229/marketing-board-strategy.jpg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$0.",
          value: "00",
          descrition: "CORSO COPYWRITING: SCRIVERE PER VENDERE",
          free: true,
          lessons: "2 lessons",
          students: "800 students",
        },
        {
          img: "https://images.pexels.com/photos/590016/pexels-photo-590016.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          price: "$50.",
          value: "00",
          free: false,
          descrition:
            "Web Marketing 4.0: il corso completo di digital marketing",
          lessons: "5 lessons",
          students: "50 students",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
body {
  font-family: "Montserrat";
}
</style>
