<template lang="html">
  <footer>
   <p>ToDoList.pl Dominik Jecek 2018 &copy; Wszelkie prawa zastrzeżone</p>
 </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
footer{
    padding: 20px;
    bottom: 0;
    width: 100%;
    min-height: 60px;
    background-color:#343a40;
    margin-top: 30px;
}
p{
  text-align: center;
  color: white;
}
</style>
