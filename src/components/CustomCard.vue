<template>
  <div class="cc-card">
    <img class="icon" src="../assets/logo.png" alt="avatar" />
    <h3>{{ data.title }}</h3>
    <p>
      {{ data.description }}
    </p>
  </div>
</template>

<script>
export default {
  name: "CustomCard",
  props: ["data"],
  methods: {
    markDone() {
      this.$emit("done", this.data);
    },
  },
};
</script>

<style>
.icon {
  height: 30px;
}
.cc-card {
  padding: 10px;
  text-align: left;
  border: 1px solid #dbdbdb;
  border-radius: 5px;
  box-shadow: 1px 1px 1px 1px rgb(161, 161, 163);
  margin: 5px;
  background-color: white;
  min-width: 200px;
  font-size: 0.8em;
}

.cc-card h3 {
  margin: 0px;
}

.cc-btn {
  background-color: #5cdb95;
  border: none;
  color: white;
  border-radius: 5px;
}
</style>
