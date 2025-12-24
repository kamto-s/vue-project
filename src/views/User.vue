<template>
  <h1>Ini Halaman User</h1>
  <ul>
    <li v-for="user in users">
      <RouterLink :to="'/user/' + user.params">
        {{ user.name }}
      </RouterLink>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { params: "andy", name: "andy" },
        { params: "anto", name: "anto" },
        { params: "yati", name: "yati" },
      ],
    };
  },
};
</script>
