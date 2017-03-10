<template>
  <div id="app">

    <h1 v-html="title"></h1>
    <input v-model="newItem" v-on:keyup.enter="addNew" placeholder="edit here">
    <div>{{content}}</div>
    <section>
      <ul>
        <li v-for="item in items"
        v-bind:class="{finished: item.isFinished}" v-on:click="clickFinished(item)">
          {{item.label}}
        </li>
      </ul>
      <p>child do something to father: {{childsay}}</p>
    </section>
    <Componenta msgfromFather='wake up' v-on:childDo="act"></Componenta>
  </div>
</template>

<script>
import Store from './store'
import Componenta from './components/ComponentA'
export default {
  data () {
    return {
      title: '<span>love</span>Vue.js',
      content: 'This is my first vue menu list',
      items: Store.fetch(),
      newItem: '',
      childsay: ''
    }
  },
  methods: {
    clickFinished: function (item) {
      item.isFinished = !item.isFinished
    },
    addNew: function () {
      this.items.push({
        label: this.newItem,
        isFinished: false
      })
      this.newItem = ''
      Store.save()
    },
    act: function (msg) {
      this.childsay = msg
    }
  },
  watch: {
    items: {
      handler: function (items) {
        Store.save(items)
      },
      deep: false
    }
  },
  components: {
    Componenta
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f40;
  margin-top: 60px;
}
.finished {
  text-decoration:underline;
  border:1px blue;
  font-size:16px;
}
li{
  cursor:pointer;
  font-size:20px;
  text-decoration: none;
}
</style>
