<template>
  <section class="container" :style="'background-color:' + bgColor + ''">

    <div class="left-side padded-left">

      <div class="button" @click="this.toggleButton">
        <div class="button-inner" :style="'box-shadow:' + toggleButtonBoxShadow + ';'">
          <div class="button-toggle" :style="'left:' + togglePosition + 'px' + '; background-color:' + toggleButtonColor + ';'"></div>
        </div>
      </div>

      <Navigation :linkColor="this.linkColor"/>



      <div class="page-container">

      <div class="content">



      <nuxt />

      </div>

      </div>



    </div>


    <div class="right-side">
      <div class="colored-box" :style="'background-color:' + this.boxColor"></div>
    </div>

  </section>
</template>

<script>
import Navigation from '../components/Navigation.vue';

export default {
  data() {
    return {
      page: 'index',
      boxColor: '#98EFBD',
      togglePosition: 1,
      darkMode: false,
//      toggleButtonColor: '#ACADAD',
      toggleButtonColor: '#ea7e7e',
      toggleButtonBoxShadow: '1px 1px 1px #D3D3D3',
      bgColor: 'white',
      titleColor: 'black',
      currentPage: '',
      linkColor: '#707070',
      media: [],
    }
  },


  computed: {

  },

  components: {
    Navigation
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
          this.togglePosition = 19;
          this.bgColor = 'black';
          this.titleColor = 'grey';
          this.boxColor = '#175A5A';
          this.linkColor = '#175A5A';
//          this.toggleButtonColor = '#ACADAD';
          this.toggleButtonColor = '#175A5A';
          this.toggleButtonBoxShadow = 'initial'
      },

      lightModeProperties() {
          this.togglePosition = 1;
          this.bgColor = 'white';
          this.titleColor = 'black';
          this.boxColor = '#98EFBD';
          this.linkColor = '#707070';
//          this.toggleButtonColor = '#ACADAD';
          this.toggleButtonColor = '#ea7e7e';
          this.toggleButtonBoxShadow = '1px 1px 1px #D3D3D3';
      },

      isItLate() {
          if(new Date().getHours() > 20) {
              return this.activateDarkMode();
          }
      }
  },

  created() {
      this.isItLate();

      let css = "text-shadow: 2px 2px rgb(0, 255, 99); font-size: 24px; font-family: sans-serif";

      console.log("%c\n\nMy senses tell me you must be some sort of super coder! 😎 \n\nI have open-sourced all of the code for this site, feel free to fork the repository:\n\nhttps://github.com/sunil-sandhu/sunilsandhu2019-nuxt\n\n\n\n", css);

  },


}


</script>

<style>

html {
  font-family: 'IBM Plex Sans', 'Helvetica Neue', 'Helvetica', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, Arial, sans-serif;
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
  /* justify-content: left; */
  align-items: flex-end;
  /* text-align: left; */
  /* width: 100%; */
  /* padding: 10px; */
   transition: all 350ms;
}

.sidebar {
  /*width: 100px;*/
  margin-left: 40px;
  display: flex;
  /* align-items: center; */
  /* justify-content: center; */
  /*height: calc(100vh - 20px);*/
  /* padding-top: 10%; */
  padding-bottom: 34px;
}

.padded-bottom {
  padding-bottom: 20px;
}

.col-2 {
  width: 50%;
  flex-flow: column;
  display: flex;
  /*align-items: flex-end;*/
}


.left-side {
  position: relative;
  width: 60%;
  flex-flow: column;
  display: flex;
  /*align-items: flex-end;*/
}

.right-side {
  width: 40%;
  flex-flow: column;
  display: flex;
  /*align-items: flex-end;*/
}

.padded-left {
  padding-left: 100px;
}

.content {
  display: flex;
  flex-flow: column;
  /*padding: 0 20px;*/
  justify-content: space-between;
}

.button {
  cursor: pointer;
  position: absolute;
  top: 20px;
  left: 20px;
  /*border: 1px solid rgba(169, 169, 169, 0.5);*/
  width: 46px;
  height: 28px;
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button-inner {
  cursor: pointer;
  position: relative;
  width: 42px;
  height: 24px;
  border: 1px solid #2e2e2e;
  border-radius: 15px;
  display: flex;
  align-items: center;
  /*background-color: #D3D3D3;*/
  transition: all 400ms;
  box-shadow: 1px 1px 1px #D3D3D3;
}

.button-toggle {
  cursor: pointer;
  position: absolute;
  width: 20px;
  height: 20px;
  top: 1px;
  border: 1px solid #2e2e2e;
  /*box-shadow: 1px 1px 1px rgb(175, 173, 173);*/
  border-radius: 15px;
  transition: all 200ms;
}

.navigation {
  display: flex;
  /*padding-left: 80px;*/
}

.navigation a {
  height: 30px;
  padding-top: 22px;
  margin-right: 20px;
  font-size: 18px;
}

.page-container {
  height: calc(100vh - 30px);
  display: flex;
  align-items: center;

}


.big {
  font-size: 1.5em;
  color: #4B4B4B;
}

a {
  text-decoration: none;
  text-align: left;
  color: rgb(86, 107, 140);
  cursor: pointer;
}

.name {
  /*margin-top: 100px;*/
  /*text-orientation: sideways;*/
  /*writing-mode: vertical-rl;*/
  /*transform: rotate(-180deg);*/
  font-size: 2.5em;
}

h1 {
  /*opacity: 0;*/
  font-size: 3em;
  font-weight: 500;
  color: #3B3B3B;
  /*animation: fadeIn 0.5s linear 0.2s forwards;*/
}

h2 {
  /*opacity: 0;*/
  font-size: 2em;
  font-weight: 500;
  color: #646464;
  /*animation: fadeIn 0.4s linear 0.7s forwards;*/
}

.tagline {
  margin-bottom: 20px;
}

.learn-more {
  margin-bottom: 100px;
  /*opacity: 0;*/
  animation: colorfulFadeIn 3s linear 1.3s forwards;
  color: #606060;
  border: 1px solid #2e2e2e;
  padding: 6px 12px;
  /* margin-top: 50px; */
  border-radius: 6px;
  transition: all 400ms;
  box-shadow: 1px 1px 1px #2e2e2e;
}

.learn-more:hover {
  box-shadow: 1px 1px 1px  rgb(23, 90, 90);
  border: 1px solid rgb(23, 90, 90);
  color: rgb(23, 90, 90);
}

.text-container {
  padding-right: 60px;
  max-height: 600px;
  overflow-x: scroll;
  max-width: 500px;
}

.colored-box {
  width: 100%;
  height: 100vh;
  height: -webkit-fill-available;
  transition: all 350ms;
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


@keyframes colorfulFadeIn {
  0% {
  }
  25% {
    border-color: #2d4f68;
  }
  50% {
    border-color: #2d4f68;
  }
  75% {
    border-color: #4b5e6c;
  }
  100% {
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



@media only screen and (max-width: 799px) {

  .left-side {
    width: 70%;
    flex-flow: column;
    display: flex;
    /*align-items: flex-end;*/
  }

  .right-side {
    width: 30%;
    flex-flow: column;
    display: flex;
    /*align-items: flex-end;*/
  }

  .padded-left {
    padding-left: 50px;
  }

  .button {
    left: unset;
    right: 20px;
  }

}



@media only screen and (max-width: 499px) {

  .container {
    flex-wrap: wrap;
  }

  .left-side {
    width: 100%;
    flex-flow: column;
    display: flex;
    height: calc(100vh - 40px);
    /*align-items: flex-end;*/
  }

  .right-side {
    width: 100%;
    flex-flow: column;
    display: flex;
    height: 40px;
    /*align-items: flex-end;*/
  }

  .padded-left {
    padding-left: 0;
  }

  .button {
    left: unset;
    right: 20px;
  }

  .text-container {
    padding: 0 20px 40px 20px;
  }

  .navigation {
    padding-left: 20px;
    background-color: rgb(239, 239, 239);
    height: 60px;
    border-bottom: 1px solid grey;
  }

  .navigation a {
    padding-top: 18px;
  }

  .page-container {
    /*height: unset;*/
  }

  .button {
    top: 16px;
  }

  .content {
    display: unset;
    flex-flow: unset;
    padding: unset;
    justify-content: unset;
  }

}

</style>
