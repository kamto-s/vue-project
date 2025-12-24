<template>
  <p>Hello World!</p>
  <hr />
  <Student @response="showData" studentName="Andy"> ini slot dari parent 1 </Student>
  <Student @response="showData" studentName="Bob"></Student>
  <Student @response="showData" studentName="Charlie"></Student>
  <p>Student yang dipilih adalah : {{ selectedStudent }}</p>
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
    showData(whatever) {
      this.selectedStudent = whatever;
      console.log(whatever);
    },
  },
};
</script>
