<template>
  <div class="about">
    <div class="container">
      <NavComponent></NavComponent>
      <TestComponent></TestComponent>
      <h1>This is an about page</h1>

      <div class="row">
        <div class="col-md-6">mmmm</div>
        <div class="col-md-6">mmmm</div>
      </div>
    </div>
  </div>
</template>
<script>
import NavComponent from "@/components/NavComponent.vue";
import TestComponent from "@/components/TestComponent.vue";
export default {
  el: "#about",
  name: "TestView",
  components: {
    TestComponent,
    NavComponent,
  },
  metaInfo() {
    return {
      title: "About",
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
