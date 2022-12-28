<template>
<!--  <button class="btn">Add Task</button>-->
  <button v-on:click="onclick()" v-bind:style="{background: color}" class="btn">{{ text }}</button>
<!--  instead of v-bind: we can only write : & in place of v-on: we can write @ -->
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    color: String
  },
  methods: {
    onclick() {

    }
  }
}
</script>