<template>
  <div class="home">

    <Header msg="Welcome to Your Vue.js App"/>
    <Main/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'home',
  components: {
    Header,
    Main
  }
}
</script>
