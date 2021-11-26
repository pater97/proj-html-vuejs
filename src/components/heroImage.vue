<template>
  <div class="hero_image container-fluid d-flex flex-column align-items-center">
    <!-- testo  -->
    <h5>Commence Buisness</h5>
    <h1>Distant Mentoring Program</h1>
    <!-- bottone download  -->
    <div class="btn_download">
      <button>
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
      </button>
    </div>
    <div class="side_menu d-flex flex-column">
        <img src="../assets/icon/ruler-combined-solid.svg" alt="">
        <img src="../assets/icon/expand-arrows-alt-solid.svg" alt="">
        <img src="../assets/icon/book-solid.svg" alt="">
        <img src="https://icon-library.com/images/cart-icon-png/cart-icon-png-0.jpg" alt="">
    </div>
  </div>
</template>
 

<style lang="scss" scoped>
@import "./colori.scss";
.hero_image {
  background-image: url(../assets/principal/home-3-hero-bg.jpg);
  position: relative;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 11rem 0;
  color: white;
  text-align: center;
  h1{
      font-size: 3rem;
      font-weight: 300;
      margin-bottom: 1.5rem;
  }
  .btn_download{
      button{
          padding: .8rem 3rem;
          color: $brandColor;
          font-weight: bolder;
          background-color: white;
          border: none;
          border-radius: 5px;
          line-height: 1rem;
          &:hover{
              color: white;
              background-color: $brandColor;
              transform: scale(110%);
              transition: all 1s;
          }
      }
      svg{
          width: 1rem;
      }
  }
  .side_menu{
      position: absolute;
      background-color: white;
      border-radius: 10px 0px 0px 10px;
      padding: .3rem;
      right: 0;
      top: 20%;
      img{
          width: 1rem;
          margin: .5rem 0;
          &:hover{
              cursor: pointer;
          }
      }
  }
}
</style>