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

</style>
