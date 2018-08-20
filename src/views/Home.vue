<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <h1>{{ message2 }}</h1>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Mike changed the message.",
      message2: "Elizabeth added a message."
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>