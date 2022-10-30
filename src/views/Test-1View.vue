<template>
  <div id="test-1">
    <div class="container">
      <NavComponent></NavComponent>
      <h1>This is Test 1 Page</h1>
      <div v-html="htmlcontent"></div>
      <div>{{ htmlcontent }}</div>
      <p>Message is: {{ message }}</p>
      <input v-model="message" placeholder="edit me" />
      <input type="checkbox" id="checkbox" v-model="checked" />
      <label for="checkbox">{{ checked }}</label>
      <div>Checked names: {{ checkedNames }}</div>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
      <label for="jack">Jack</label>

      <input type="checkbox" id="john" value="John" v-model="checkedNames" />
      <label for="john">John</label>

      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
      <label for="mike">Mike</label>
      <form id="signup-form">
        <div class="row">
          <div class="col-12 form-group">
            <label class="col-form-label col-form-label-lg"
              >Full Name <span class="text-danger">*</span></label
            >
            <input type="text" class="form-control form-control-lg" />
          </div>
          <div class="col-12 form-group">
            <label class="col-form-label col-form-label-lg"
              >Email <span class="text-danger">*</span></label
            >
            <input type="email" class="form-control form-control-lg" />
          </div>
          <div class="col-12 form-group">
            <label class="col-form-label col-form-label-lg"
              >Country <span class="text-danger">*</span></label
            >
            <select class="form-control form-control-lg">
              <option value="">Select Country</option>
            </select>
          </div>
          <div class="col-12 form-group">
            <label class="col-form-label col-form-label-lg"
              >Password <span class="text-danger">*</span></label
            >
            <input type="password" class="form-control form-control-lg" />
          </div>
          <div class="col-12 form-group text-center">
            <button class="btn btn-vue btn-lg col-4">Sign Up</button>
          </div>
        </div>
      </form>
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
      message: "  ",
      checked: true,
      checkedNames: [],
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
<style>
.btn-vue {
  background: #53b985;
  color: #31485d;
  font-weight: bold;
}
</style>
