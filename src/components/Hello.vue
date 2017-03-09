<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">貂蝉d</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">吕布</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">荆轲</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">花木兰</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">王者荣耀</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">阴阳师</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">三国杀</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">穿越火线</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: '这里放文字~'
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
#hello {
  color:#ff00ff;
}
</style>
