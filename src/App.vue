<template>
  <div id="app">
    <ul class="links">
      <li>
        <router-link to="/" exact>HOME</router-link>
      </li>
      <li>
        <router-link to="/about">ABOUT</router-link>
      </li>
      <li>
        <router-link to="/detail">DETAIL</router-link>
      </li>
      <li>
        <router-link to="/nest">NEST</router-link>
      </li>
    </ul>

    <div class="page">
      <transition name="router">
        <roure-view/>
      </transition>
    </div>
  </div>
</template>

<script>
export default{
  name: "App"
};
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}

#app {
  margin: 0;
  padding: 0;
}

.links {
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
  display: flex;
  list-style: none;
}

.links > li a:hover {
  background: #f6f6f6;
}

.links > li > a.router-link-active {
  background: ransparent;
  color: teal;
  cursor: defalt;
}

.page {
  position: relative;
}

.page > *{
  position: absolute;
}

.router-enter-active{
  transition: all 1s;
  transition-delay: 0.5s;
}

.router-leave-active{
  transition: all 0.5s;
}

.router-enter,
.router-leave-to{
  opacity: 0;
}
</style>
