<template>
  <div id="app">
    <Header class="mar-bottom-std"></Header>
    <div class="body-container">
      <div class="left-column">
        <div class="mar-bottom-small placeholder-for-separator" v-if="!showSeparator1"></div>
        <transition name="fade">
          <Separator class="mar-bottom-small" :inverse="true" v-if="showSeparator1"></Separator>
        </transition>
        <Skills class="mar-bottom-std"></Skills>
        <div class="mar-bottom-small placeholder-for-separator" v-if="!showSeparator2"></div>
        <transition name="fade">
          <Separator class="mar-bottom-small" :inverse="true" v-if="showSeparator2"></Separator>
        </transition>
        <Experience class="mar-bottom-std" ></Experience>
      </div>
      <div class="right-column">
        <div class="mar-bottom-small placeholder-for-separator" v-if="!showSeparator3"></div>
        <transition name="fade">
          <Separator class="mar-bottom-small" :inverse="true" v-if="showSeparator3"></Separator>
        </transition>
        <Education class="mar-bottom-std" ></Education>
        <div class="mar-bottom-small placeholder-for-separator" v-if="!showSeparator4"></div>
        <transition name="fade">
          <Separator class="mar-bottom-small" :inverse="true" v-if="showSeparator4"></Separator>
        </transition>
        <Personal-info class="mar-bottom-std" ></Personal-info>
        <div class="mar-bottom-small placeholder-for-separator" v-if="!showSeparator5"></div>
        <transition name="fade">
          <Separator class="mar-bottom-small" :inverse="true" v-if="showSeparator5"></Separator>
        </transition>
        <Profile class="mar-bottom-std" ></Profile>
      </div>
    </div>
  </div>
</template>

<script>
const timeFirstSeparatorToAppear = 500
const timeDelay = 150

import Header from './components/Header.vue'
import PersonalInfo from './components/PersonalInfo.vue'
import Separator from './components/Separator.vue'
import Profile from './components/Profile.vue'
import Skills from './components/Skills.vue'
import Experience from './components/Experience.vue'
import Education from './components/Education.vue'

export default {
  name: 'app',
  components: {
    Header,
    PersonalInfo,
    Separator,
    Profile,
    Skills,
    Experience,
    Education
  },
  data() {
    return {
      showSeparator1: false,
      showSeparator2: false,
      showSeparator3: false,
      showSeparator4: false,
      showSeparator5: false,
    }
  },
  mounted() {
    setTimeout(function() {
      this.showSeparator1 = true
    }.bind(this), timeFirstSeparatorToAppear)
    setTimeout(function() {
      this.showSeparator2 = true
    }.bind(this), timeFirstSeparatorToAppear + timeDelay)
    setTimeout(function() {
      this.showSeparator3 = true
    }.bind(this), timeFirstSeparatorToAppear + (timeDelay * 2))
    setTimeout(function() {
      this.showSeparator4 = true
    }.bind(this), timeFirstSeparatorToAppear + (timeDelay * 3))
    setTimeout(function() {
      this.showSeparator5 = true
    }.bind(this), timeFirstSeparatorToAppear + (timeDelay * 4))
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Nunito+Sans:400,500,600,700,800&display=swap');
@import './styles/reset.css';
@import './styles/common.scss';
#app {
  font-family: 'Nunito Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $black;
  background-color: $app-background;
  min-height: 100vh;
  padding: $app-padding;
}
.placeholder-for-separator {
  border-bottom: $separators-width solid transparent;
}
.fade-enter-active, .fade-leave-active {
  transition: all 1s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  transform: translateX(300px);
  opacity: 0;
}
@media (min-width: 768px) {
  .body-container {
    display: flex;
    .left-column {
      flex-basis: 60%;
      margin-right: 1rem;
    }
    .right-column {
      flex-basis: 40%;
    }
  }
}
</style>
