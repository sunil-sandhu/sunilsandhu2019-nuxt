<template>
  <section class="container" :style="'background-color:' + bgColor + ''">

    <div class="button" @click="this.toggleButton">
      <div class="button-inner">
        <div class="button-toggle" :style="'left:' + togglePosition + 'px' + '; background-color:' + toggleButtonColor + ';'"></div>
      </div>
    </div>

    <div class="col-2 padded-bottom">

      <div class="sidebar">
        <h1 class="name" :style="'color:' + this.titleColor">sunil sandhu</h1>
      </div>


      <nuxt/>
    </div>


    <div class="col-2">
      <div class="colored-box" :style="'background-color:' + this.boxColor"></div>
    </div>

  </section>
</template>

<script>
export default {
  data() {
    return {
      page: 'index',
      boxColor: '#98EFBD',
      togglePosition: 0,
      darkMode: false,
      toggleButtonColor: '#ACADAD',
      bgColor: 'white',
      titleColor: 'black',
      currentPage: '',
    }
  },

  computed: {

  },

  components: {

  },

  methods: {



      toggleButton() {
          if(! this.darkMode) {
              this.activateDarkMode();
          } else {
              this.activateLightMode();
          }
      },

      activateDarkMode() {
          this.darkMode = true;
          this.darkModeProperties();
      },

      activateLightMode() {
          this.darkMode = false;
          this.lightModeProperties();
      },

      darkModeProperties() {
          this.togglePosition = 20;
          this.bgColor = 'black';
          this.titleColor = 'grey';
          this.boxColor = '#175A5A';
//          this.toggleButtonColor = '#175A5A';
      },

      lightModeProperties() {
          this.togglePosition = 0;
          this.bgColor = 'white';
          this.titleColor = 'black';
          this.boxColor = '#98EFBD';
//          this.toggleButtonColor = '#ACADAD';
      },

      isItLate() {
          if(new Date().getHours() > 20) {
              return this.activateDarkMode();
          }
      }
  },

  created() {
      this.isItLate();

  },


}


</script>

<style>

html {
  font-family: 'Helvetica Neue', 'Helvetica', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  text-align: left;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}


.container {
  min-height: 100vh;
  display: flex;
  justify-content: left;
  align-items: flex-end;
  text-align: left;
  width: 100%;
  padding: 10px;
  transition: all 350ms;
}

.sidebar {
  width: 100px;
  margin-left: 40px;
}

.padded-bottom {
  padding-bottom: 20px;
}

.col-2 {
  width: 50%;
  display: flex;
  align-items: flex-end;
}

.content {
  display: flex;
  flex-flow: column;
  padding: 0 20px;
}

.button {
  position: absolute;
  top: 50px;
  left: 50px;
  border: 1px solid darkgrey;
  width: 60px;
  height: 30px;
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button-inner {
  position: relative;
  width: 56px;
  height: 26px;
  border: 1px solid grey;
  border-radius: 15px;
  display: flex;
  align-items: center;
  background-color: #D3D3D3;
}

.button-toggle {
  position: absolute;
  width: 34px;
  height: 24px;
  top: 0;
  border: 1px solid #707070;
  border-radius: 15px;
  transition: all 350ms;
}

nuxt-link {
}

.big {
  font-size: 1.5em;
  color: #4B4B4B;
}

a {
  text-decoration: underline;
  text-align: left;
  color: #707070;
}

.name {
  margin-top: 100px;
  text-orientation: sideways;
  writing-mode: vertical-rl;
  transform: rotate(-180deg);
}

h1 {
  font-size: 3em;
  color: #343434;
}

h2 {
  font-size: 2em;
  color: #646464;
}

.tagline {
  margin-bottom: 10px;
}

.learn-more {
  margin-bottom: 100px;

}

.text-container {
  padding-right: 100px;
}

.colored-box {
  width: 100%;
  height: calc(100vh - 20px);
  height: -webkit-fill-available;
  transition: all 500ms;
}


.fade-in {
  animation: fadeIn 0.4s ease-in-out forwards;
}

@keyframes fadeIn {
  0% {
    opacity: 0;

  }
  100% {
    opacity: 1;

  }
}


/*TRANSITIONS START*/
.page-enter-active {
  animation: acrossIn 0.6s ease-out both;
}

.page-leave-active {
  animation: acrossOut 0.6s ease-in both;
}

@keyframes acrossIn {
  0% {
    opacity: 0;
    /*transform: translate3d(100%, 0, 0);*/
  }
  100% {
    opacity: 1;
    /*transform: translate3d(0, 0, 0);*/
  }
}

@keyframes acrossOut {
  0% {
    opacity: 1;
    /*transform: translate3d(0, 0, 0);*/
  }
  100% {
    opacity: 0;
    /*transform: translate3d(-100%, 0, 0);*/
  }
}
/*TRANSITIONS END*/



@media only screen and (max-width: 999px) {
}

</style>
