<template>
  <div>
    <p class="title">Json Online Comparer</p>
    <div class="files">
      <div class="file file1">
        <p>Content A:</p>
        <textarea v-model="oldStr"></textarea>
      </div>
      <div class="file file2">
        <p>Content B:</p>
        <textarea v-model="newStr"></textarea>
      </div>
    </div>
    <div>
      <code-diff
        :old-string="oldStr"
        :new-string="newStr"
        :context="30"
        outputFormat="side-by-side"
      />
    </div>
  </div>
</template>

<script>
import CodeDiff from "vue-code-diff";
export default {
  name: "App",
  components: { CodeDiff },
  data() {
    return {
      oldStr: `{
      "Name":"bmw 2002",
      "Miles_per_Gallon":26,
      "Cylinders":4,
      "Displacement":121,
      "Horsepower":113,
      "Weight_in_lbs":2234,
      "Acceleration":12.5,
      "Year":"1970-01-01",
      "Origin":"Europe"
   }`,
      newStr: `{
      "Name":"bmw 320i",
      "Miles_per_Gallon":21.5,
      "Cylinders":4,
      "Displacement":121,
      "Horsepower":110,
      "Weight_in_lbs":2600,
      "Acceleration":12.8,
      "Year":"1977-01-01",
      "Origin":"Europe"
   }`,
    };
  },
};
</script>

<style>
@import "./assets/styles.css";
</style>
