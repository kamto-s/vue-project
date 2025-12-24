<template>
  <p>Hello World!</p>
  <hr />
  <Student @response="showData" studentName="Andy" />
  <Student @response="showData" studentName="Bob" />
  <Student @response="showData" studentName="Charlie" />
  <p>Student yan dipilih adalah : {{ selectedStudent }}</p>
</template>

<script>
import Student from "./components/Student.vue";
export default {
  components: {
    Student,
  },
  data() {
    return {
      selectedStudent: "",
    };
  },
  methods: {
    showData(student) {
      this.selectedStudent = student;
    },
  },
};
</script>
