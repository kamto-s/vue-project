<template>
  <p>
    Component Student <strong>{{ studentName }} <button @click="showData">click me</button></strong>
  </p>
</template>

<script>
export default {
  props: {
    studentName: String,
  },
  emits: ["response"],
  methods: {
    showData() {
      this.$emit("response", this.studentName);
    },
  },
};
</script>
