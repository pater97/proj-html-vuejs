<template>
  <div class="container_header d-flex justify-content-between align-items-center p-3">
    <!-- menù di sinistra  -->
    <section class="left d-flex align-items-center">
      <div class="hidden_hamburger">
        <div class="collapse" id="navbarToggleExternalContent">
          <div class="p-4">
            <h5 class="h4">Collapsed content</h5>
            <span class="text-muted">Toggleable via the navbar brand.</span>
          </div>
        </div>
        <nav class="navbar navbar-dark">
          <div class="container-fluid">
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarToggleExternalContent"
              aria-controls="navbarToggleExternalContent"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
          </div>
        </nav>
      </div>
      <div v-for="link in navBar" :key="link.name">
        <div class="header_link" @click="getLink()">
          {{link.name}} 
          <span>
            <img :src="link.chevron" alt="">
          </span>
          <div class="dropdown">
            <a>{{link.dd1}}</a>
            <a>{{link.dd2}}</a>
            <a>{{link.dd3}}</a>
          </div>
        </div>
      </div>
    </section>
    <!-- menu di sinistra -->
    <!-- logo -->
    <div class="logo">
      <img src="../assets/icon/dark-logo.png" alt="" />
    </div>
    <!-- /logo  -->
    <!-- menù di destra  -->
    <div class="right d-flex align-items-center justify-content-end">
      <!-- carrello shopping  -->
      <div class="cart">
        <img
          src="https://icon-library.com/images/cart-icon-png/cart-icon-png-0.jpg"
          alt=""
        />
        <div class="items_on_cart">0</div>
      </div>
      <!-- account icon  -->
      <div class="account">
        <img src="../assets/icon/user-circle-regular.svg" alt="" />
      </div>
      <!-- barra di ricerca  -->
      <div class="search_bar">
        <input type="text" placeholder="Search..." />
        <svg
          aria-hidden="true"
          focusable="false"
          data-prefix="fas"
          data-icon="search"
          class="svg-inline--fa fa-search fa-w-16"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M505 442.7L405.3 343c-4.5-4.5-10.6-7-17-7H372c27.6-35.3 44-79.7 44-128C416 93.1 322.9 0 208 0S0 93.1 0 208s93.1 208 208 208c48.3 0 92.7-16.4 128-44v16.3c0 6.4 2.5 12.5 7 17l99.7 99.7c9.4 9.4 24.6 9.4 33.9 0l28.3-28.3c9.4-9.4 9.4-24.6.1-34zM208 336c-70.7 0-128-57.2-128-128 0-70.7 57.2-128 128-128 70.7 0 128 57.2 128 128 0 70.7-57.2 128-128 128z"
          ></path>
        </svg>
      </div>
    </div>
    <!-- /menu di destra  -->
  </div>
</template>

<script>
export default {
  props:{
    navBar:Array
  },
  data(){
    return{
    }
  }
}

</script>


<style lang="scss" scoped>
@import "./colori.scss";
// ampiezze
.left,
.right,
.logo {
  width: calc(100% / 3);
  text-align: center;
}
// menù di sinistra
.left {
  .hidden_hamburger{
      display: none;
      .navbar{
          background-color: $brandColor;
          border-radius: 30px;
      }
      .navbar-dark{
          color: $brandColor;
      }
  }
  .header_link{
    margin-right: .7rem;
    position: relative;
    &:hover{
      color: $brandColor;
      cursor: pointer;
    }
    &:hover .dropdown{
          display: flex;
          flex-direction: column;
          align-items: center;
    }
    span{
      img{
        width: .5rem;
      }
    }
    .dropdown{
      display: none;
      position: absolute;
      z-index: 10;
      width: 6rem;
      left: 1rem;
      background-color: $brandColor;
      text-align: center;
      a{
        color: white;
        width: 100%;
        &:hover{
          background-color: #3f3a64;
        }
      }
    }
  }
}
// logo
.logo {
  img {
    width: 11rem;
  }
}
// menù di dstra
.right {
  .cart,
  .account {
    margin: 0 1rem;
    img {
      width: 1.2rem;
    }
  }
  .cart {
    position: relative;
    .items_on_cart {
      position: absolute;
      top: -1rem;
      background-color: $brandColor;
      top: -0.2rem;
      border-radius: 50%;
      right: -0.7rem;
      height: 0.8rem;
      width: 0.8rem;
      line-height: 0.7rem;
      color: white;
      font-size: 0.7rem;
    }
  }
  .search_bar {
    background-color: #f5f5f5;
    padding: 0.5rem 1rem;
    border-radius: 10px;
    input {
      border: none;
      background-color: transparent;
      width: 80%;
    }
    svg {
      width: 1rem;
      color: $brandColor;
    }
  }
}
@media screen and (max-width: 1279px) {
  .left {
    .dropdown {
      display: none;
    }
    .hidden_hamburger{
        display: block;
    }
  }
  .right{
      .search_bar{
          width: 5rem;
      }
  }
}
@media screen and (min-width: 1440px){
.container_header{
    width: 1440px;
    margin: auto;
}
}
</style>