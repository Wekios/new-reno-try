<template>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/mybusiness">My Business</router-link>
      <img src="../../assets/logo.png">
      <router-link to="/myvan">My van</router-link> |
      <router-link to="/about">About</router-link>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
#nav {
  padding: 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 60%;
  margin: 0 auto;

  img {
    width: 10rem;
  }

  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

</style>