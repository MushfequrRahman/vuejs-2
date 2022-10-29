<template>
  <div class="test">
    <div class="container">
      <NavComponent></NavComponent>
      <TestComponent></TestComponent>
      <ContentComponent></ContentComponent>
      <h1 v-show="show">This is test page</h1>
      <h1 v-show="show1">This is test page................</h1>
      <h2>{{ msg() }}</h2>
      <button v-on:click="say('hi')">Say Hi</button>
      <div class="container">
        <div class="row">
          <div class="col-md-6">mmmm</div>
          <div class="col-md-6">mmmm</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import NavComponent from "@/components/NavComponent.vue";
import TestComponent from "@/components/TestComponent.vue";
import ContentComponent from "@/components/ContentComponent.vue";
export default {
  el: "#test",
  name: "TestView",
  components: {
    TestComponent,
    ContentComponent,
    NavComponent,
  },
  data: function () {
    return {
      show: true,
      show1: true,
    };
  },
  methods: {
    say: function (msg) {
      alert(msg);
    },
    msg: function () {
      return "Welcome to this tutorial on ";
    },
  },
};
</script>
