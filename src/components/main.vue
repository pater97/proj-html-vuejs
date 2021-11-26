<template>
  <div class="container">
    <!-- sezione inerente alla 'work culture' con dati -->
    <section id="work_culture">
      <div class="row">
        <!-- colonna di sinistra con testo -->
        <div class="text col-md-6 d-flex">
          <!-- sezione di solo testo  -->
          <div class="left_text col-9">
            <h6>EVERYTHING IN <span>MAXCOACH</span></h6>
            <h2>
              Learn about our <span class="brand_color">Work Culture</span> at
              Max coach
            </h2>
            <p>
              Spend some time to visit our website or head office and discover
              our current courses, enrollment procedure, and registration
              deadline. We are opening new classes every beginning of each
              month.
            </p>
            <p>
              Have questions?
              <span class="brand_color">
                Get free guide
                <svg
                  aria-hidden="true"
                  focusable="false"
                  data-prefix="fas"
                  data-icon="long-arrow-alt-right"
                  class="svg-inline--fa fa-long-arrow-alt-right fa-w-14"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 448 512"
                >
                  <path
                    fill="currentColor"
                    d="M313.941 216H12c-6.627 0-12 5.373-12 12v56c0 6.627 5.373 12 12 12h301.941v46.059c0 21.382 25.851 32.09 40.971 16.971l86.059-86.059c9.373-9.373 9.373-24.569 0-33.941l-86.059-86.059c-15.119-15.119-40.971-4.411-40.971 16.971V216z"
                  ></path></svg
              ></span>
            </p>
          </div>
          <!--forma geometrica nella colonna di sinistra  -->
          <div class="right_shape col-3">
            <svg
              aria-hidden="true"
              focusable="false"
              data-prefix="far"
              data-icon="circle"
              class="svg-inline--fa fa-circle fa-w-16"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
            >
              <path
                fill="currentColor"
                d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm0 448c-110.5 0-200-89.5-200-200S145.5 56 256 56s200 89.5 200 200-89.5 200-200 200z"
              ></path>
            </svg>
          </div>
        </div>
        <!-- colonna di destra con immagini  -->
        <div class="work_culture_image col-md-6">
          <img
            class="principal_image"
            src="../assets/principal/work_culture-1.jpg"
            alt=""
          />
          <img
            class="secondary_image"
            src="../assets/principal/work-culture-2.jpg"
            alt=""
          />
          <img
            class="geometric_shape"
            src="../assets/shape/maxcoach-shape-02.png"
            alt=""
          />
          <img
            class="square_shape"
            src="../assets/shape/maxcoach-shape-07.png"
            alt=""
          />
        </div>
        <div class="dati"></div>
      </div>
    </section>
    <!-- sezione con i dati dei risultati  -->
    <section id="dati" class="d-flex justify-content-center text-center">
      <!-- colonna di sinistra  -->
      <div class="col-md-3">
        <h2 class="brand_color fw-bold">129+</h2>
        <h6>ENROLLED LEARNES</h6>
      </div>
      <!-- colonna centrale  -->
      <div class="col-md-3">
        <h2 class="brand_color fw-bold">80</h2>
        <h6>FINISHED SESSION</h6>
      </div>
      <!-- colonna destra  -->
      <div class="col-md-3">
        <h2 class="brand_color fw-bold">4%</h2>
        <h6>SATISFACTION RATE</h6>
      </div>
    </section>
    <!-- sezione "upgrade your skills" -->
    <section id="upgrade_skills">
      <div class="row">
        <div class="col-md-6 upgrade_image position-relative">
          <div class="upgrade_principal">
            <img
              class="upgrade_principal_image"
              src="../assets/principal/upgrade-principal.jpg"
              alt=""
            />
            <img
              class="youtube_play"
              src="../assets/icon/icon-youtube-play.png"
              alt=""
            />
          </div>
          <img class="up_shape_radius" src="../assets/shape/mc5.png" alt="" />
          <img class="up_shape_square" src="../assets/shape/mc7.png" alt="" />
        </div>
        <div class="col-md-6 upgrade_text">
          <h6>HOW WE WORK</h6>
          <h2>
            Upgrade Your Skills
            <span class="brand_color">Upgrade Your life</span>
          </h2>
          <p>
            Opening up more opportunities in front of you to get the ticket to
            more enjoyable door in info. Getting equipped with new skills for
            new sets of insights into your career.Maxcoach accompany in every
            stage of learning.
          </p>
          <div>
            Download free guidebook
            <svg
              aria-hidden="true"
              focusable="false"
              data-prefix="fas"
              data-icon="long-arrow-alt-right"
              class="svg-inline--fa fa-long-arrow-alt-right fa-w-14"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 448 512"
            >
              <path
                fill="currentColor"
                d="M313.941 216H12c-6.627 0-12 5.373-12 12v56c0 6.627 5.373 12 12 12h301.941v46.059c0 21.382 25.851 32.09 40.971 16.971l86.059-86.059c9.373-9.373 9.373-24.569 0-33.941l-86.059-86.059c-15.119-15.119-40.971-4.411-40.971 16.971V216z"
              ></path>
            </svg>
          </div>
        </div>
      </div>
    </section>
    <!-- sezione anteprima corsi  -->
    <section id="courses">
      <!-- titolo -->
      <div class="title_section text-center">
        <h6>JOIN MAXCOACH AT THE BEST</h6>
        <h2>Lastes Online <span class="brand_color">Courses</span></h2>
      </div>
      <!-- gruppo slide 1 -->
      <div class="row" v-show="array1">
        <div class="col-md-4" v-for="corso in corsiSlide1" :key="corso.value">
          <div class="image">
            <img src="../assets/courses/slide.jpg" alt="" />
            <div class="free" v-show="corso.free">FREE</div>
          </div>
          <div class="info">
            <div class="price brand_color">
              <h5>
                {{ corso.price }}<span>{{ corso.value }}</span>
              </h5>
            </div>
            <div class="descrition">
              <p>{{ corso.descrition }}</p>
            </div>
            <div class="info_numbers d-flex justify-content-around">
              <h6>
                 <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="book" class="svg-inline--fa fa-book fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"></path></svg>
                 {{ corso.lessons }}
              </h6>
              <h6>
                <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="user" class="svg-inline--fa fa-user fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"></path></svg>
                {{ corso.students }}
              </h6>
            </div>
          </div>
        </div>
      </div>
      <!-- gruppo slide 2 -->
       <div class="row" v-show="array2">
        <div class="col-md-4" v-for="corso in corsiSlide2" :key="corso.value">
          <div class="image">
            <img src="../assets/courses/slide.jpg" alt="" />
            <div class="free" v-show="corso.free">FREE</div>
          </div>
          <div class="info">
            <div class="price brand_color">
              <h5>
                {{ corso.price }}<span>{{ corso.value }}</span>
              </h5>
            </div>
            <div class="descrition">
              <p>{{ corso.descrition }}</p>
            </div>
            <div class="info_numbers d-flex justify-content-around">
              <h6>
                 <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="book" class="svg-inline--fa fa-book fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"></path></svg>
                 {{ corso.lessons }}
              </h6>
              <h6>
                <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="user" class="svg-inline--fa fa-user fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"></path></svg>
                {{ corso.students }}
              </h6>
            </div>
          </div>
        </div>
      </div>
      <!-- gruppo slide 3 -->
       <div class="row" v-show="array3">
        <div class="col-md-4" v-for="corso in corsiSlide3" :key="corso.value">
          <div class="image">
            <img src="../assets/courses/slide.jpg" alt="" />
            <div class="free" v-show="corso.free">FREE</div>
          </div>
          <div class="info">
            <div class="price brand_color">
              <h5>
                {{ corso.price }}<span>{{ corso.value }}</span>
              </h5>
            </div>
            <div class="descrition">
              <p>{{ corso.descrition }}</p>
            </div>
            <div class="info_numbers d-flex justify-content-around">
              <h6>
                 <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="book" class="svg-inline--fa fa-book fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"></path></svg>
                 {{ corso.lessons }}
              </h6>
              <h6>
                <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="user" class="svg-inline--fa fa-user fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"></path></svg>
                {{ corso.students }}
              </h6>
            </div>
          </div>
        </div>
      </div>
      <!-- pallini per navigare nelle slide  -->
      <div class="scroll_slide">
        <div :class="{'active':array1}" @click="getSlideOne"></div>
        <div :class="{'active':array2}" @click="getSlideTwo"></div>
        <div :class="{'active':array3}" @click="getSlideThree"></div>
      </div>
      <div class="all_courses col-md-5">
        <p>
          Control your personal preference settings to get notifed about appropiate courses.
           <a href="#">
             View all courses
             <svg
                  aria-hidden="true"
                  focusable="false"
                  data-prefix="fas"
                  data-icon="long-arrow-alt-right"
                  class="svg-inline--fa fa-long-arrow-alt-right fa-w-14"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 448 512"
                >
                  <path
                    fill="currentColor"
                    d="M313.941 216H12c-6.627 0-12 5.373-12 12v56c0 6.627 5.373 12 12 12h301.941v46.059c0 21.382 25.851 32.09 40.971 16.971l86.059-86.059c9.373-9.373 9.373-24.569 0-33.941l-86.059-86.059c-15.119-15.119-40.971-4.411-40.971 16.971V216z"
                  ></path></svg>
           </a>
        </p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      array1:true,
      array2:false,
      array3:false,
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
          img: "",
          price: "$0.",
          value: "00",
          descrition: "Customer-Centric info-Tech Strategist",
          free: true,
          lessons: "24 lessons",
          students: "769 students",
        },
        {
          img: "",
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
          img: "slide.jpg",
          price: "$0.",
          free: true,
          value: "00",
          descrition: "Corso completo di Data Science e machine learning con Python",
          lessons: "40 lessons",
          students: "10 students",
        },
        {
          img: "",
          price: "$12.",
          value: "00",
          descrition: "Guida Pratica e Completa a Django, Python e Bootstrap",
          free: false,
          lessons: "5 lessons",
          students: "300 students",
        },
        {
          img: "",
          price: "$30.",
          value: "00",
          free: false,
          descrition: "Social Media Marketing - Il Corso Completo con Certificato",
          lessons: "7 lessons",
          students: "70 students",
        },
      ],
      corsiSlide3: [
        {
          img: "slide.jpg",
          price: "$110.",
          free: false,
          value: "00",
          descrition: "FACEBOOK ADS GURU 2021 - Corso operativo completo",
          lessons: "10 lessons",
          students: "30 students",
        },
        {
          img: "",
          price: "$0.",
          value: "00",
          descrition: "CORSO COPYWRITING: SCRIVERE PER VENDERE",
          free: true,
          lessons: "2 lessons",
          students: "800 students",
        },
        {
          img: "",
          price: "$50.",
          value: "00",
          free: false,
          descrition: "Web Marketing 4.0: il corso completo di digital marketing",
          lessons: "5 lessons",
          students: "50 students",
        },
      ],
    };
  },
  methods:{
    getSlideOne(){
      this.array1 =  true
      this.array2 = false
      this.array3 = false
    },
    getSlideTwo(){
      this.array1 =  false
      this.array2 = true
      this.array3 = false
    },
    getSlideThree(){
      this.array1 =  false
      this.array2 = false
      this.array3 = true
    }
  },
};
</script>

<style lang="scss" scoped>
@import "./colori.scss";
.brand_color {
  color: $brandColor;
}
// impostazioni comuni
.text,
.work_culture_image {
  padding: 8rem 0;
  position: relative;
}
.square_shape,
.geometric_shape,
.secondary_image {
  position: absolute;
}
// sezione colonna di testo
.text {
  .left_text {
    h2 {
      font-size: 3rem;
    }
    h6 {
      color: $greyText;
      span {
        font-weight: bolder;
        color: #6e6b69;
      }
    }
    p {
      span {
        font-weight: bolder;
        &:hover {
          text-decoration: underline;
          cursor: pointer;
        }
        svg {
          width: 1rem;
        }
      }
    }
  }
  .right_shape {
    width: 3rem;
    color: #ecc5ab;
  }
}
// sezione immagini
.work_culture_image {
  &:hover .geometric_shape {
    transform: rotate(360deg);
    transition: all 3s;
  }
  .principal_image {
    width: 90%;
    z-index: 2;
    position: relative;
  }
  .secondary_image {
    top: 4rem;
    right: 0;
    width: 10rem;
    border-radius: 5px;
    z-index: 10;
  }
  .geometric_shape {
    bottom: 6.2rem;
    right: 7rem;
    width: 6rem;
    z-index: 10;
  }
  .square_shape {
    z-index: 1;
    width: 8rem;
    top: 5rem;
    right: 5rem;
  }
}
// SEZIONE CON DATI
#dati {
  h6 {
    color: #6e6b69;
    font-size: 0.7rem;
    font-weight: bold;
  }
}
// sezione upgrade skills
#upgrade_skills {
  padding: 8rem 0;
  // sezione con immagini 
  .upgrade_image {
    .upgrade_principal {
      position: relative;
      width: 100%;
      z-index: 10;
      .upgrade_principal_image {
        width: 100%;
        border-radius: 10px;
        box-shadow: 2px 14px 20px 0px #625e5e;
        &:hover {
          filter: brightness(0.5);
        }
      }
      .youtube_play {
        position: absolute;
        top: 40%;
        left: 40%;
        &:hover {
          cursor: pointer;
        }
      }
    }
    .up_shape_radius,
    .up_shape_square {
      position: absolute;
      width: 9rem;
    }
    .up_shape_radius {
      top: 3rem;
      left: -5rem;
      z-index: 1;
    }
    .up_shape_square {
      bottom: -4rem;
      right: -1rem;
      z-index: 1;
    }
  }
  // sezione con testo 
  .upgrade_text {
    padding-left: 5rem;
    h6,
    p {
      color: $greyText;
    }
    h2 {
      font-size: 3.5rem;
      padding-bottom: 1rem;
    }
    div {
      font-weight: bold;
      &:hover {
        text-decoration: underline;
        cursor: pointer;
      }
      svg {
        width: 1rem;
      }
    }
  }
}
// sezione corsi
#courses {
  // paragrafo con titoli 
  .title_section {
    h6 {
      color: $greyText;
      font-size: 0.8rem;
    }
    h2 {
      font-weight: bold;
      font-size: 2.3rem;
      span {
        font-weight: 400;
      }
    }
  }
  // impostazioni slide 
  .row {
    .col-md-4:hover .descrition{
      color: $brandColor;
    }
    .image {
      margin: 4rem 0 1rem 0;
      position: relative;
      .free {
        position: absolute;
        top: 0;
        right: 0;
        background-color: #ee7455;
        color: white;
        padding: 0.1rem 0.5rem;
      }
      img {
        width: 100%;
        border-radius: 5px;
      }
    }
    .info {
      padding: 1rem;
      .price {
        h5 {
          font-weight: bolder;
          span {
            font-size: 0.8rem;
          }
        }
      }
      .descrition {
        font-weight: bolder;
        font-size: 1.2rem;
        color: #565656;
      }
    }
    .info_numbers {
      h6 {
        color: #ADACBD;
        font-size: .8rem;
        svg{
          width: .8rem;
        }
      }
    }
  }
  // impostazioni per pallini di navigazione slide 
  .scroll_slide{
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 2rem;
    .active{
      background-color:  $brandColor;
      height: 1rem;
      width: 1rem;
    }
    div{
      height: .7rem;
      width: .7rem;
      border-radius: 50%;
      background-color: lightgrey;
      margin: .5rem;
      &:hover{
        cursor: pointer;
        box-shadow: 0px 0px 5px 1px $brandColor;
      }
    }
  }
  // paragrafo per link a tutti i corsi 
  .all_courses{
    text-align: center;
    margin: auto;
    p{
      font-weight: 500;
      color: $greyText;
    }
    a{
      color: black;
      text-decoration: none;
      font-weight: bold;
      &:hover{
        text-decoration: underline $brandColor;
      }
      svg{
        width: 1rem;
      }
    }
  }
}
</style>