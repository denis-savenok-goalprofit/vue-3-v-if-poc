<template>
  <div>
    <button @click="onClick">{{ this.title }}</button>
  </div>
</template>

<script>
export default {
  props: {
    title: {type: String}
  },

  data() {
    return {
      _uid: this.$.uid
    }
  },

  created() {
    console.log('Test created', this._uid);
  },

  mounted() {
    console.log('Test mounted', this._uid);
  },

  unmounted() {
    console.log('Test unmounted', this._uid);
  },

  methods: {
    onClick() {
      console.log('UID', this._uid);
    }
  }
}
</script>