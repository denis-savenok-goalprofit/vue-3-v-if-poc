<template>
  <div>
    <div v-if="someCondition">
      <Test ref="one" :title="title" />
    </div>
    <div v-else>
      <Test ref="two" :title="title_1" />
    </div>
    <button @click="onClick">Switch components!</button>
  </div>
</template>

<script>
import Test from './test.vue'

export default {
  components: { Test },

  data() {
    return {
      title: 'title',
      title_1: 'title_1',
      someCondition: true
    }
  },

  methods: {
    onClick() {
      this.someCondition = !this.someCondition
    }
  }
}
</script>