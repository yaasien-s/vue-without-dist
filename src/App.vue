<template>
  <div id="nav">
    <router-link to="/" title="HOME">Home</router-link> |
    <router-link to="/about" title="ABOUT">About</router-link> |
    <router-link to="/resume" title="RESUME">Resume</router-link> |
    <router-link to="/proj" title="PROJECTS">Projects</router-link> |
    <router-link to="/contact" title="CONTACT">Contact</router-link>
  </div>
    <router-view v-slot="{ Component }">
      <transition name="route" mode="out-in">
        <component :is="Component"></component>
      </transition>
    </router-view>

    <!-- <Footer />   -->

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2b2b26;
}

#nav {
  padding: 30px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
}

nav ul {
  text-align: center;
  background: linear-gradient(90deg, rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, 0.2) 25%, rgba(255, 255, 255, 0.2) 75%, rgba(255, 255, 255, 0) 100%);
  box-shadow: 0 0 25px rgba(0, 0, 0, 0.1), inset 0 0 1px rgba(255, 255, 255, 0.6);
}

#nav a {
  font-weight: bold;
  color: #fff;
  text-decoration: none;
  padding: 8px;
  border-radius: 4px;
  font-weight: 500;
  font-size: 1.1rem;
  box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
}

#nav a.router-link-exact-active {
  color: #568259;
  background: #2b2b26;
  letter-spacing: 2px;
  transition: 0.4s;
  font-weight: 300;
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


/* route transition */
.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}
.route-enter-active {
  transition: all 0.3s ease-out;
}
.route-leave-to {
  opacity: 0;
  transform: translateX(-100px);
}
.route-leave-active {
  transition: all 0.3s ease-in;
}
@media (max-width: 550px) {
  #nav a {
    padding: 3px;
    font-size: 10px;
  }
  #nav a.router-link-exact-active {
    letter-spacing: 0;
  }
}

</style>
