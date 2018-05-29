<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://github.com/vuejs/vue-cli/tree/dev/docs" target="_blank">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org/en/essentials/getting-started.html" target="_blank">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org/en/intro.html" target="_blank">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org/en" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
  <div>
    <g>
      <polygon :points="points"></polygon>
      <axis-lable v-for="(stat, index) in stats"></axis-lable>
    </g>
  </div>
</template>

<script>
Vue.component('polygraph', {
  props: ['stats'],
  template: '#polygraph-template',
  computed: {
    points: function()
  },
  components: {
    'axis-lable': {
      props: {
        stat: Object,
        index: Number,
        total: Number
      },
    template: '#axis-label-template',
      computed: {}
    }
  }
})

new Vue({
  el: '#demo',
  data: {
    newLabel: '',
    stats: stats
  },
  methods: {
    add: function () {
    },
    remove: function () {
    }
  }
})

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }

  const delay = seconds => new Promise(resolve => setTimeout(resolve, seconds*1000))

  return {
    [Symbol.asyncInterator]: async function*() {
      let pageIndex = 1
      while(true){
      const pageData = await tagSearch(tag, pageIndex)
      for(const url of pageData){
        await delay(2)
        yield url
      }
      pageIndex = pageIndex + 1
      }
    }
  }
}

let pattern1 = "{[()]}"
let patter2 = "/\{\[\(\)\]\}\/"
let flags = "gim"
let cleanup1 = new RegExp(pattern1, flags)
let cleanup2 = new RegExp(pattern2, flags)

pattern1.match(pattern2)
pattern2.replace()
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
