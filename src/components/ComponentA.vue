<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{msg2}}</h2>
    <strong>{{msgfromFather}}</strong></br>
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
      // console.log(this.msgfromFather)
      this.$emit('childDo', this.msg)
      // this.$dispatch('childDo', this.msg)// dispatch在2.0中被废弃
      this.msg = ''
    }
  },
  props: ['msgfromFather']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  color:#a43253;
}

</style>
