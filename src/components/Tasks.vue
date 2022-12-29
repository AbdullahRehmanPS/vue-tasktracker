<template>
  <div v-bind:key="task.id" v-for="task in tasks">
<!--    <h3>{{task.text}}</h3>-->
    <Task @toggle-reminer="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" v-bind:task="task"/>
  </div>
</template>

<script>
import Task from "@/components/Task";
export default {
  name: 'Tasks',
  components: {Task},
  props: {
    tasks: Array
  },
  emits: ['delete-task','toggle-reminder']
}
</script>