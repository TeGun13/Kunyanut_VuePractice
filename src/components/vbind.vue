<template>
  <div>
    <h1>V-Bind</h1>
    <button
      v-bind:class="{ green: check, blue: !check }"
      v-on:click="check = !check"
    />

    <h1 v-if="(check = check)">This is true</h1>
    <h1 v-else>This is false</h1>
  </div>
</template>  

<script>
export default {
  data() {
    return {
      check: true,
    };
  },
};
</script>


<style>
.green {
  background-color: palegreen;
  width: 100px;
  height: 100px;
}
.blue {
  background-color: mediumblue;
  width: 100px;
  height: 100px;
}
</style>