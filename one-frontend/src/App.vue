<template>
  <div id="app">
    <router-view name="navbar"></router-view>
    <transition name="slide" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import "animate.css";
export default {
  components: {
    NavBar
  }
};
</script>

<style>
#app {
  padding: 0;
  font-family: "Open Sans", sans-serif;
  display: grid;
  grid-template-columns: 15em auto;
  grid-template-areas: "navBar dashboard";
  background-color: #f7f7fc;
}
.slide-enter-active {
  transition-duration: 0.3s;
  transition-property: all;
  transition-timing-function: ease;
}
.slide-leave-active {
  transition-duration: 0.2s;
  transition-property: all;
  transition-timing-function: ease;
}

.slide-enter {
  opacity: 0;
  transform: translateY(100px);
}
.slide-leave-to {
  opacity: 0;
  transform: translateY(-100px);
}

/* Global Styles */
html,
body {
  padding: 0;
  margin: 0;
}
/* screen on the right */
.first-background {
  background-color: #f7f7fc;
  padding: 2em 2.8em;
  min-height: 100vh;
}
h1 {
  font-size: 2.5em;
  margin-top: 0;
  margin-bottom: 0;
  font-weight: 800;
  color: #222;
}
h2 {
  margin: 0;
  font-size: 1.5em;
  text-transform: uppercase;
  color: #414141;
  margin-bottom: 15px;
}
h3 {
  margin: 0;
}
.subtitle {
  font-size: 1.1em;
  font-weight: 700;
  color: #909090;
}
.second-background {
  box-sizing: border-box;
  background-color: white;
  width: 100%;
  padding: 2em;
  margin: 1.3em 0;
  border-radius: 2em;
}
.bubble {
  background-color: #f9f9fa;
  border-radius: 10px;
}
/* Other elements */
hr {
  background-color: #d0d0d0;
  height: 4px;
  border: none;
  border-radius: 5px;
}
button {
  padding: 8px 20px;
  border: none;
  background-color: #ebebeb;
  color: #909090;
  font-weight: 700;
  font-size: 1em;
  font-family: "Segoe UI";
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s ease;
}
button:focus {
  outline: 0;
}
.disabled {
  background-color: #ebebeb !important;
  color: #909090 !important;
  cursor: default !important;
}
input {
  padding: 8px 20px;
  border: none;
  background-color: #ebebeb;
  color: #4f4f4f;
  font-weight: 700;
  font-size: 1em;
  font-family: "Segoe UI";
  border-radius: 30px;
  box-sizing: border-box;
}
input:focus {
  outline: 0;
}
</style>
