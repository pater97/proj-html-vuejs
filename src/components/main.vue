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
          <div class="card">
            <div class="image">
              <img :src="require(`../assets/courses/${corso.img}`)" alt="" />
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
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="fas"
                    data-icon="book"
                    class="svg-inline--fa fa-book fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"
                    ></path>
                  </svg>
                  {{ corso.lessons }}
                </h6>
                <h6>
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="far"
                    data-icon="user"
                    class="svg-inline--fa fa-user fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"
                    ></path>
                  </svg>
                  {{ corso.students }}
                </h6>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- gruppo slide 2 -->
      <div class="row" v-show="array2">
        <div class="col-md-4" v-for="corso in corsiSlide2" :key="corso.value">
          <div class="card">
            <div class="image">
              <img :src="corso.img" alt="" />
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
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="fas"
                    data-icon="book"
                    class="svg-inline--fa fa-book fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"
                    ></path>
                  </svg>
                  {{ corso.lessons }}
                </h6>
                <h6>
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="far"
                    data-icon="user"
                    class="svg-inline--fa fa-user fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"
                    ></path>
                  </svg>
                  {{ corso.students }}
                </h6>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- gruppo slide 3 -->
      <div class="row" v-show="array3">
        <div class="col-md-4" v-for="corso in corsiSlide3" :key="corso.value">
          <div class="card">
            <div class="image">
              <img :src="corso.img" alt="" />
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
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="fas"
                    data-icon="book"
                    class="svg-inline--fa fa-book fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M448 360V24c0-13.3-10.7-24-24-24H96C43 0 0 43 0 96v320c0 53 43 96 96 96h328c13.3 0 24-10.7 24-24v-16c0-7.5-3.5-14.3-8.9-18.7-4.2-15.4-4.2-59.3 0-74.7 5.4-4.3 8.9-11.1 8.9-18.6zM128 134c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm0 64c0-3.3 2.7-6 6-6h212c3.3 0 6 2.7 6 6v20c0 3.3-2.7 6-6 6H134c-3.3 0-6-2.7-6-6v-20zm253.4 250H96c-17.7 0-32-14.3-32-32 0-17.6 14.4-32 32-32h285.4c-1.9 17.1-1.9 46.9 0 64z"
                    ></path>
                  </svg>
                  {{ corso.lessons }}
                </h6>
                <h6>
                  <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="far"
                    data-icon="user"
                    class="svg-inline--fa fa-user fa-w-14"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      fill="currentColor"
                      d="M313.6 304c-28.7 0-42.5 16-89.6 16-47.1 0-60.8-16-89.6-16C60.2 304 0 364.2 0 438.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-25.6c0-74.2-60.2-134.4-134.4-134.4zM400 464H48v-25.6c0-47.6 38.8-86.4 86.4-86.4 14.6 0 38.3 16 89.6 16 51.7 0 74.9-16 89.6-16 47.6 0 86.4 38.8 86.4 86.4V464zM224 288c79.5 0 144-64.5 144-144S303.5 0 224 0 80 64.5 80 144s64.5 144 144 144zm0-240c52.9 0 96 43.1 96 96s-43.1 96-96 96-96-43.1-96-96 43.1-96 96-96z"
                    ></path>
                  </svg>
                  {{ corso.students }}
                </h6>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- pallini per navigare nelle slide  -->
      <div class="scroll_slide">
        <div :class="{ active: array1 }" @click="getSlideOne"></div>
        <div :class="{ active: array2 }" @click="getSlideTwo"></div>
        <div :class="{ active: array3 }" @click="getSlideThree"></div>
      </div>
      <div class="all_courses col-md-5">
        <p>
          Control your personal preference settings to get notifed about
          appropiate courses.
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
              ></path>
            </svg>
          </a>
        </p>
      </div>
    </section>
    <!-- sezione testimonianze  -->
    <section id="testimonials">
      <div class="row">
        <div class="col-md-4">
          <h6>TESTIMONIALS</h6>
          <h2>Why Do People <span class="brand_color">*Hearts*</span> Us?</h2>
          <p>
            Seeking for verbals of our service quality? Find them here. <br />
            Everyting is trasparent and straightforward for your sense of
            justification.
          </p>
          <p>
            View all
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
          </p>
        </div>
        <div class="col-md-8">
          <div class="card bottom">
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. lorem
              asuhfabas xhnhasusni ejsja riebna fdeo e ifdweinwe ii
            </p>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit.
              Perferendis numquam sint corporis, at tempore quo nihil molestiae
              illo dolorem laudantium, repudiandae eos aperiam deserunt libero
              facilis sed magni! Suscipit illum quam ullam praesentium illo
              doloremque sed veritatis eaque? Aspernatur, obcaecati et ipsa
              dicta quaerat nam tempora repellat quia exercitationem illum
              laudantium odit explicabo, possimus aut sequi voluptatibus vel
              voluptas ullam fugit commodi id nisi accusamus. A quos odio
              aliquid! Facere eligendi quis inventore quam atque suscipit
              numquam praesentium accusamus, quae animi deleniti adipisci
              minima! Hic id odit tempore dolor asperiores obcaecati qui rerum
              ratione reprehenderit officia commodi, adipisci repellat unde?
            </p>
            <div class="avatar">
              <img src="../assets/avatar/testimonial-avata-02.jpg" alt="" />
            </div>
          </div>
          <div class="card top">
            <p class="fw-bold">
              Professional team of specialists and passionate moentors at reach
            </p>
            <p class="text-muted">
              i need to get a certification for English proficency and MaxCoach
              is my best choiche. Their tutors are smarth and professional when
              dealing whit students.
            </p>
            <div class="avatar d-flex">
              <img src="../assets/avatar/testimonial-avata-01.jpg" alt="" />
              <div class="avatar_info">
                <h6 class="fw-bold">Madley Pondor</h6>
                <p class="text-muted">/ IT Specialist</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- sezione guida -->
    <section id="guida">
      <div class="row">
        <div class="left col-md-6">
          <img
            class="team_img"
            src="../assets/avatar/home-3-team-image.png"
            alt=""
          />
          <img
            class="mc_shape"
            src="../assets/shape/maxcoach-shape-01.png"
            alt=""
          />
          <img class="mc5" src="../assets/shape/mc5.png" alt="" />
          <img class="mc7" src="../assets/shape/mc7.png" alt="" />
        </div>
        <div class="right col-md-6">
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
          <div class="info_text">
            <h6>EVERYTHING IN <span class="fw-bolder">MAXCOACH</span></h6>
            <h2>
              We're Here to <br />
              <span class="brand_color">Transform</span> You!
            </h2>
            <p class="text-muted">
              As learnes,people can enjoy great compionship from br MaxCoach
              menthors and educators.We can help you develop and grow at your
              best
            </p>
            <button>Get Free Guide</button>
          </div>
        </div>
      </div>
    </section>
    <!-- seizione blog -->
    <section id="blog">
      <div class="blog_title">
        <h6 class="text-muted">
          READ FOR MORE JOYMENT
        </h6>
        <h2>
          Lastes from <span class="brand_color">Our Blogs</span>
        </h2>
      </div>
      <div class="row">
        <div class="col-md-4" v-for="blog in slideBlog" :key="blog.descrition">
          <div class="card">
            <div class="image">
              <img :src="require(`../assets/courses/${blog.img}`)" alt="" />
            </div>
            <div class="info">
              <h5>
                ARTIST
              </h5>
              <div class="descrition">
                <p>{{ blog.descrition }}</p>
              </div>
              <div class="info_numbers d-flex">
                <h6>
                  <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="calendar" class="svg-inline--fa fa-calendar fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M400 64h-48V12c0-6.6-5.4-12-12-12h-40c-6.6 0-12 5.4-12 12v52H160V12c0-6.6-5.4-12-12-12h-40c-6.6 0-12 5.4-12 12v52H48C21.5 64 0 85.5 0 112v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V112c0-26.5-21.5-48-48-48zm-6 400H54c-3.3 0-6-2.7-6-6V160h352v298c0 3.3-2.7 6-6 6z"></path></svg>
                  {{ blog.date }}
                </h6>
                <h6>
                  <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="eye" class="svg-inline--fa fa-eye fa-w-18" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path fill="currentColor" d="M288 144a110.94 110.94 0 0 0-31.24 5 55.4 55.4 0 0 1 7.24 27 56 56 0 0 1-56 56 55.4 55.4 0 0 1-27-7.24A111.71 111.71 0 1 0 288 144zm284.52 97.4C518.29 135.59 410.93 64 288 64S57.68 135.64 3.48 241.41a32.35 32.35 0 0 0 0 29.19C57.71 376.41 165.07 448 288 448s230.32-71.64 284.52-177.41a32.35 32.35 0 0 0 0-29.19zM288 400c-98.65 0-189.09-55-237.93-144C98.91 167 189.34 112 288 112s189.09 55 237.93 144C477.1 345 386.66 400 288 400z"></path></svg>
                  {{ blog.views }}
                </h6>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- sezione newsletter -->
    <section id="newsletter" class="row">
      <div class="col-md-3 circle_shape">
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
      <div class="col-md-6 text_newsletter">
        <h2>
        Subscribe <span class="brand_color">Newsletter</span>
      </h2>
      <p>
        Enter your email adress to register to our newsletter subscriptiondelivered on a regular basis!
      </p>
      <div class="input">
        <input type="text" placeholder="Enter your email">
        <button>Subscribe</button>
      </div>
      </div>
      <div class="col-md-3 shapes">
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
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      array1: true,
      array2: false,
      array3: false,
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
      slideBlog:[
        {
          img:'artist1.jpeg',
          descrition:'Brush Stokes Energize Trees in Paintings',
          date:'May 15,2020',
          views:'688 Views'
        },
         {
          img:'artist2.jpg',
          descrition:'Poket-sized Notebook Hold Miniature Paintings',
          date:'May 15,2020',
          views:'603 Views'
        },
         {
          img:'artist3.jpg',
          descrition:'Connection Beetween Self-portraits And Identity',
          date:'May 15,2020',
          views:'397 Views'
        },
      ]
    };
  },
  methods: {
    getSlideOne() {
      this.array1 = true;
      this.array2 = false;
      this.array3 = false;
    },
    getSlideTwo() {
      this.array1 = false;
      this.array2 = true;
      this.array3 = false;
    },
    getSlideThree() {
      this.array1 = false;
      this.array2 = false;
      this.array3 = true;
    },
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
    margin-top: 2rem;
    .col-md-4:hover .descrition {
      color: $brandColor;
    }
    .col-md-4:hover .card {
      transform: scale(105%);
    }
    .card {
      border: none;
      background-color: rgba(228, 228, 228, 0.404);
    }
    .image {
      position: relative;
      height: 14rem;
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
        height: 100%;
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
        color: #adacbd;
        font-size: 0.8rem;
        svg {
          width: 0.8rem;
        }
      }
    }
  }
  // impostazioni per pallini di navigazione slide
  .scroll_slide {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 2rem;
    .active {
      background-color: $brandColor;
      height: 1rem;
      width: 1rem;
    }
    div {
      height: 0.7rem;
      width: 0.7rem;
      border-radius: 50%;
      background-color: lightgrey;
      margin: 0.5rem;
      &:hover {
        cursor: pointer;
        box-shadow: 0px 0px 5px 1px $brandColor;
      }
    }
  }
  // paragrafo per link a tutti i corsi
  .all_courses {
    text-align: center;
    margin: auto;
    p {
      font-weight: 500;
      color: $greyText;
    }
    a {
      color: black;
      text-decoration: none;
      font-weight: bold;
      &:hover {
        text-decoration: underline $brandColor;
      }
      svg {
        width: 1rem;
      }
    }
  }
}
// sezione testimonianze
#testimonials {
  margin: 5rem 0;
  // colonna di sinistra
  .col-md-4 {
    align-self: center;
    h6,
    p {
      color: $greyText;
    }
    h2 {
      font-size: 3rem;
    }
    p:last-child {
      color: black;
      font-weight: bold;
      &:hover {
        text-decoration: underline;
      }
      svg {
        width: 1rem;
      }
    }
  }
  // colonna di destra
  .col-md-8 {
    position: relative;
    .bottom {
      width: 60%;
      margin: auto;
      padding: 2rem;
      box-shadow: 0px 0px 20px 0px grey;
      border: none;
      filter: opacity(0.3);
      position: relative;
      z-index: 1;
      .avatar {
        img {
          width: 5rem;
          border-radius: 50%;
        }
      }
    }
    .top {
      padding: 2rem;
      position: absolute;
      z-index: 2;
      top: 33%;
      font-size: 1.3rem;
      border: none;
      box-shadow: 0px 0px 20px 0px rgb(194, 194, 194);
      .avatar {
        align-items: center;
        img {
          width: 5rem;
          border-radius: 50%;
          margin-right: 1rem;
        }
      }
    }
  }
}
// sezione guida
#guida {
  margin: 10rem 0;
  // sezione di sinistra
  .left:hover .mc5 {
      transform: rotate(360deg);
      transition: all 3s;
    }
    .left:hover .mc7{
      transform: translateY(3rem);
      transition: all 3s;
    }
  .left,
  .team_img {
    position: relative;
    display: flex;
    justify-content: end;
    .team_img {
      width: 25rem;
      z-index: 2;
    }
    .mc5,
    .mc7,
    .mc_shape {
      position: absolute;
      z-index: 1;
    }
    .mc5,
    .mc7 {
      width: 8rem;
    }
    .mc_shape {
      left: 0;
      bottom: 0;
    }
    .mc5 {
      top: 20%;
      left: 20%;
    }
    .mc7 {
      width: 8rem;
      bottom: -5rem;
      right: 8rem;
    }
  }
  // sezione di destra
  .right {
    svg{
      width: 3rem;
      color: #ECC5AB;
      margin-bottom: 2rem;
    }
    .info_text{
      width: 80%;
      margin: auto;
      h6 {
        color: $greyText;
      }
      h2 {
        font-size: 3rem;
      }
      button {
        background-color: $brandColor;
        color: white;
        font-weight: bold;
        border: none;
        border-radius: 5px;
        padding: 1rem 3rem;
        margin: 1rem 0;
      }
    }
  }
}
// sezione blog
#blog{
  .blog_title{
    text-align: center;
    margin: 5rem 0;
    h2{
      font-size: 3rem;
      font-weight: bold;
    }
  }
  .row {
    margin-top: 2rem;
    .col-md-4:hover .descrition {
      color: $brandColor;
    }
    .col-md-4:hover .card {
      transform: translateY(-2rem);
      transition: all 2s;
    }
    .card {
      border: none;
      background-color: rgba(228, 228, 228, 0.404);
    }
    .image {
      height: 14rem;
      img {
        width: 100%;
        height: 100%;
        border-radius: 5px;
      }
    }
    .info {
      padding: 1rem;
      h5{
        color: $greyText;
        font-size: .8rem;
      }
      .descrition {
        font-weight: bolder;
        font-size: 1.2rem;
      }
    }
    .info_numbers {
      align-items: center;
      h6 {
        color:#565656;
        font-size: 0.8rem;
        margin-right: 2rem;
        svg {
          width: 0.8rem;
        }
      }
    }
  }
}
// sezione newsletter
#newsletter{
  margin: 3rem 0;
  .circle_shape,.text_newsletter,.shapes{
    display: flex;
  }
  .circle_shape{
    align-items: center;
    svg{
      width: 3rem;
      color: $brandColor;
    }
  }
  .text_newsletter{
    flex-direction: column;
    text-align: center;
    h2{
      font-size: 2.5rem;
      font-weight: bold;
      margin-bottom: 1rem;
      span{
        font-weight: 400;
      }
    }
    p{
      margin-bottom: 2.5rem;
    }
    .input{
      height: 3rem;
      input{
        border: none;
        background-color: #F5F5F5;
        height: 100%;
        width: 80%;
        padding: 1rem;
      }
      button{
        border: none;
        background-color: $brandColor;
        color: white;
        height: 100%;
        width: 20%;
        font-weight: bold;
      }
    }
  }
  .shapes{
    position: relative;
    align-items: center;
    justify-content: center;
    img{
      width: 6rem;
      &:last-child{
        position: absolute;
        transform: rotate(200deg);
        top: 0;
        left: 3.4rem;
      }
    }
  }
}
</style>