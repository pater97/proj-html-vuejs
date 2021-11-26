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
  </div>
</template>

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
.text{
    .left_text{
        h2{
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
              &:hover{
                  text-decoration: underline;
              }
            svg {
              width: 1rem;
            }
          }
        }
    }
    .right_shape{
        width: 3rem;
        color: #ECC5AB;
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
</style>