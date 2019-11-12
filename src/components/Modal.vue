<template lang="html">
  <div class="modalForm">
        <div class="modalContainer">
          <form class="form-inline">
            <div class="form-group">
              <label for="staticEmail2" class="sr-only">Task</label>
              <input type="text"  class="form-control" id="staticEmail2" placeholder="Task" v-model="name" >
            </div>
            <div class="form-group ">
              <label for="inputPassword2" class="sr-only">Description</label>
              <input type="text" class="form-control" id="inputPassword2" placeholder="Description" v-model="nameDescription" >
            </div>
            <button type="button" class="btn btn-primary " v-on:click="update">Add Task</button>
          </form>
        </div>
        <span class="close" @click="$emit('closeModal')">&times;</span>
      </div>
</template>

<script>
export default {
  name: "Modal"
}
</script>

<style lang="scss">
.modalForm {
    width: 100%;
    height: 100%;
    position: fixed;
    display: block;
    z-index: 1;
    left: 0;
    top: 0;
    overflow: auto;
    background-color: rgba(0,0,0,0.9);
}
.modalContainer {
    height: 70%;
    padding: 50px;
    display: flex;
    align-items: center;
    margin: 100px auto auto;
    width: 80%;
    -webkit-animation-name: zoom;
    -webkit-animation-duration: 0.6s;
    animation-name: zoom;
    animation-duration: 0.6s;
    background-color: white;
    border-radius: 1px;
}
form {
    width: 100%;
    margin: auto;

    input {
        height: 50px;
    }
    button {
        width: 100%;
        margin-top: 10px;
        height: 50px;
    }
}
@-webkit-keyframes zoom {
    from {
        -webkit-transform: scale(0);
    }
    to {
        -webkit-transform: scale(1);
    }
}
@keyframes zoom {
    from {
        transform: scale(0);
    }
    to {
        transform: scale(1);
    }
}
.close {
    position: absolute;
    top: 15px;
    right: 35px;
    color: #f1f1f1 !important;
    font-size: 40px !important;
    font-weight: bold;
    transition: 0.3s;
}
.close:focus,
.close:hover {
    color: #bbb;
    text-decoration: none;
    cursor: pointer;
}
@media only screen and (max-width: 700px) {
    .modal-content {
        width: 100%;
    }
}
</style>
