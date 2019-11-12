<template>
<div class="home">
  <Modal v-if="visible === true" @closeModal="visible = false"/>
  <Header msg="Welcome to Your Vue.js App" />
  <table class="table table-striped table-dark">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">Task</th>
        <th scope="col">Description</th>
        <th scope="col">Options</th>
      </tr>
    </thead>
    <tbody>
      <Task v-for=" result in results " :task="result" :key="result.id" />
    </tbody>
  </table>
  <Add @click.native="modalOpen"/>
  <Footer />
</div>
</template>

<script>
// @ is an alias to /src
import Task from '@/components/Task.vue'
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Add from '@/components/Add.vue'
import Footer from '@/components/Footer.vue'
import axios from 'axios'
import Modal from '@/components/Modal.vue'

const API = 'http://localhost:81/apiTodolist/read.php';

export default {
  name: 'home',
  components: {
    Header,
    Main,
    Add,
    Footer,
    Task,
    Modal
  },
  data() {
    return {
      results: [],
      visible: false,
    };
  },
  methods: {
    modalOpen() {
      this.visible = true;
    },
    apiConncet() {
      axios({
          method: 'get',
          url: `${API}`,
          responseType: 'json'
        })
        .then((response) => {
          this.results = response.data;
          console.log(response.data);
        })
        .catch((error) => {
          console.log(error);
        });
    }
  },
  beforeMount() {
    this.apiConncet()
  },
}
</script>
<style lang="scss">



</style>
