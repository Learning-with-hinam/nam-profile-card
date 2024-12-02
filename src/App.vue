<!-- javascript -->
<script setup>
import { ref } from 'vue';
// const msg = '<span style="color: red; font-size:30px;">hello world</span>'

const msg = ref('hello world') // giá trị khởi tạo của msg là 'hello world'
console.log(msg.value.toUpperCase()) // 'HELLO WORLD'

const user = ref({
  avatar: 'https://images.unsplash.com/photo-1721332155545-c7a8005a2581?q=80&w=3135&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  name: 'hinam',
  location: 'Danang',
  jobTitle: 'Developer',
  university: 'Danang Uni'
})

const members = ref([
  {
    id: 1,
    name: 'Cong Thanh'
  },
  {
    id: 2,
    name: 'Lam Son'
  },
  {
    id: 3,
    name: 'Vu'
  }
])


console.log('name:', members.value)

function sayHello() {
  console.log("hello")

  members.value.push({
    id: 4,
    name: 'nam'
  })
}

// arrow function
const sayHello2 = () => {
  console.log("hello2")
}
</script>

<!-- HTML -->
<template>
  <!-- <span>this is msg: {{ msg }}</span>
  <span v-html="msg"></span> -->
  <!-- <button v-on:click="sayHello">Click me</button>

  <button @click="sayHello2">Click me2</button>

  <div @click="sayHello">test</div>
  <span>{{ msg }}</span>
  <p>
    name: {{ user.name }}
  </p>
  <p>
    location: {{ user.location }}
  </p>
  <div>
    {{ members }}
  </div> -->
  <div>
    <h2 style="text-align:center">User Profile Card</h2>

    <div class="card">
      <img :src="user.avatar" alt="John" style="width:100%">
      <h1>{{ user.name }}</h1>
      <p class="title">{{ user.jobTitle }}</p>
      <p>{{ user.university }}</p>
      <div style="margin: 24px 0;">
        <a href="#"><i class="fa fa-dribbble"></i></a>
        <a href="#"><i class="fa fa-twitter"></i></a>
        <a href="#"><i class="fa fa-linkedin"></i></a>
        <a href="#"><i class="fa fa-facebook"></i></a>
      </div>
      <p><button>Contact</button></p>
    </div>
  </div>
</template>

<!-- CSS -->
<style></style>
