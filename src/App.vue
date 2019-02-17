<template>
  <div id="app">
    <Main />
  </div>
</template>

<script>
import Main from './components/Main'

export default {
  name: 'app',
  components: {
    Main
  }
}
</script>

<style>
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}
a {
  color: #000000;
}
p {
  margin-bottom: 5px;
}
hr {
    border: none;
    height: 3px;
    /* Set the hr color */
    color: #f3f3f3; /* old IE */
    background-color: #f3f3f3; /* Modern Browsers */
    margin-bottom: -15px;
}
</style>
