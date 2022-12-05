<template>
<nav id="navbar-example2" class="navbar navbar-light bg-light px-3">
  <a class="navbar-brand" href="#">Vuelog</a>
  <ul class="nav nav-pills">
    <li class="nav-item">
      <a class="nav-link" href="#scrollspyHeading1">아무</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#scrollspyHeading2">거나</a>
    </li>
    <li class="nav-item dropdown">
      <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#" role="button" aria-expanded="false">Dropdown</a>
      <ul class="dropdown-menu">
        <li><a class="dropdown-item" href="#scrollspyHeading3">Third</a></li>
        <li><a class="dropdown-item" href="#scrollspyHeading4">Fourth</a></li>
        <li><hr class="dropdown-divider"></li>
        <li><a class="dropdown-item" href="#scrollspyHeading5">Fifth</a></li>
      </ul>
    </li>
  </ul>
</nav>
<!-- <div style="padding:20px;" data-bs-spy="scroll" data-bs-target="#navbar-example2" data-bs-offset="0" class="scrollspy-example" tabindex="0">
  
  <h4 id="scrollspyHeading1">초보 개발자 블로그</h4>
  <p>뭘봐?</p>
</div> -->
<router-link to="/list">리스트페이지</router-link>
<router-link to="/">홈페이지</router-link>

<div class="mt-4">
<router-view :blog="blog"></router-view>
</div>
<!-- <List :blog="blog[i]" v-for="(a,i) in blog" :key="i"/> -->

</template>


<script>

// import List from './components/Lists.vue';
import blog from './assets/blog.js';

export default {
  name: 'App',
  data(){
    return {
      blog : blog
    }
  },
  components: {
    // List : List,
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
