<template>
  <div class="home">
    <NavComponent></NavComponent>
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import NavComponent from "@/components/NavComponent.vue";
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    NavComponent,
  },
  metaInfo() {
    return {
      title: "Home",
      meta: [
        {
          vmid: "description",
          name: "description",
          content:
            "hello world, this is an example of adding a description with vueMeta",
        },
      ],
    };
  },
};
</script>
