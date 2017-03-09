<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{msg2}}</h2>
    <button v-on:click="onClick">click</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Hello world',
      msg2: 'Hello developer'
    }
  },
  methods: {
    onClick: function () {
      alert('111')
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  color:#a43253;
}

</style>
