<template>
<div class="todo">
    <form class="form">
      <input class="field" type="text" input="search" placeholder="search">
    </form>

    <ul class="todo-list">
      <% todo.forEach(function(todo) { %> 
      <li>
        <%= todo %>
      </li>
      <% }); %> 
    </ul>
    <transition>
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </transition>
    <Post v-for="post in posts" :post="post"></Post>
  </div>   
</template>

<script>

let pattern1 = "{[()]}"
let patter2 = "/\{\[\(\)\]\}\/"
let flags = "gim"
let cleanup1 = new RegExp(pattern1, flags)
let cleanup2 = new RegExp(pattern2, flags)

pattern1.match(pattern2)
pattern2.replace()

const ul = document.getElementsByClassName(links)
const form = document.getElementsByClassName(form)

form &&
  form.addEventListener("submit", e => 
    e.preventDefault)

import {
  thing
} from '../path/thing'

export default {
  ready(){
    this.getPage()
  },

data() {
  return {
    page: {

    }
  }
}
    
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}

.form ul> li {
  list-style: none;
}

li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.links {

}

.todo {

}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.todo-list {
  list-style: none;
  justify-content: space-between;
  justify-self: first baseline;
  display: flex;
}
</style>

