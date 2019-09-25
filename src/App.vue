<template>
  <div id="app">
    <div id="wrapper">
      <nav>
        <ul>
          <li><router-link to="/" active-class="active" exact>HOME</router-link></li>
          <li><router-link to="/about" active-class="active" exact>ABOUT</router-link></li>
        </ul>
      </nav>
      <!-- <transition name="fade" mode="out-in" appear> -->
      <transition name="slide">
        <router-view></router-view>
      </transition>
    </div>
  </div>
</template>

<style lang="scss">

  body {
    background: #eccf6f;
    margin: 0;
    padding: 0;
    overflow: hidden;
    * {
      margin: 0;
      padding: 0;
    }
  }

  .fade-enter {
    opacity: 0;
    transform: scale(0);
  }
  .fade-enter-active {
    transition: .5s;
  }
  .fade-enter-to {
    opacity: 1;
    transform: scale(1);
  }
  .fade-leave {
    opacity: 1;
    transform: scale(1);
  }
  .fade-leave-active {
    transition: .5s;
  }
  .fade-leave-to {
    opacity: 0;
    transform: scale(0);
  }

  .slide-enter {
    opacity: 0;
    transform: scale(0);
  }
  .slide-enter-active {
    transition: 2s;
  }
  .slide-enter-to {
    opacity: 1;
    transform: scale(1);
  }
  .slide-leave {
    opacity: 1;
    transform: scale(1);
  }
  .slide-leave-active {
    transition: 2s;
  }
  .slide-leave-to {
    opacity: 0;
    transform: scale(2);
  }

  @keyframes scaleUp {
    0% { transform: scale(0.8)}
    100% { transform: scale(1)}
  }


  #app {
    background: #eccf6f;
    position: relative;
    #wrapper {
      width: 100%;
      height: 100vh;
    }
  }
  
  nav {
    background: #0e2d92;
    position: relative;
    z-index: 20;
    ul {
      display: flex;
      margin: 0;
      padding: 0;
      line-height: 80px;
      height: 80px;
      li {
        list-style: none;
        margin: 0 10px;
        a {
          text-decoration: none;
          font-size: 20px;
          font-weight: bold;
          color: #eccf6f;
          &.active {
            background: #eccf6f;
            color: #0e2d92;
            padding: 5px 10px;
          }
        }
      }
    }
  }
    

  .contents {
    background: #0e2d92;
    color: #eccf6f;
    width: 100%;
    height: calc(100vh - 80px);
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;

    position: absolute;
    top: 80px;
    left: 0;
    z-index: 10;

    h1 {
      font-size: 50px;
      font-weight: bold;
    }
  }
</style>
