<template lang="html">
  <tr>
    <th>{{ id }}</th>
    <th>{{ actName }}</th>
    <th>{{ description }}</th>
    <button type="button" class="btn btn-success" >Update</button>
    <button type="button" class="btn btn-danger" >Delete</button>
  </tr>
</template>

<script>
export default {
  name: 'Task',

  props: {
    task: {
      Type: Object,
      required: true
    }
  },
  data() {
    return {
      id: this.task.id,
      actName: this.task.actName,
      description: this.task.description,
    }
  },
}
</script>

<style lang="scss">
button{
  margin: 8px;
  min-width: 100px !important;
}
</style>
