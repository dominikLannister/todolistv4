<template lang="html">
  <div class="buttonContainer">
    <button type="button" class="btn btn-primary">ADD TASK</button>
  </div>

</template>

<script>
export default {
  name: 'Add'
}
</script>

<style lang="scss" scoped>

@import url('https://fonts.googleapis.com/css?family=Oswald:400,700&display=swap');

  .buttonContainer{
    margin-top: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  button{
    font-family: 'Oswald', sans-serif;
    font-size: 50px;
    height: 80px;
    width: 80%;
    letter-spacing: 1px;
  }
</style>
