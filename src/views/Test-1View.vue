<template>
  <div id="test-1">
    <div class="container">
      <NavComponent></NavComponent>
      <h1>This is Test 1 Page</h1>
      <div v-html="htmlcontent"></div>
      <div>{{ htmlcontent }}</div>
    </div>
  </div>
</template>
<script>
import NavComponent from "@/components/NavComponent.vue";
export default {
  el: "#test-1",
  name: "Test-1View",
  components: {
    NavComponent,
  },
  data: function () {
    return {
      htmlcontent: "<div><h1>This is Vue.js Template Example</h1></div>",
    };
  },
  metaInfo() {
    return {
      title: "Test-1",
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
