<template>
  <div class="testcomponent">
    <p>For Test Page</p>
  </div>
</template>

<script>
export default {
  name: "TestComponent",
  metaInfo() {
    return {
      title: "Test",
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
