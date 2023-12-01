<template lang="">
  <form>
    <label> Email:</label>
    <input type="email" required v-model="email" />

    <label> Password:</label>
    <input type="password" required v-model="pass" />
  </form>

  <p>email:{{ email }}</p>
  <p>pass:{{ pass }}</p>
</template>
<script>
export default {
  data() {
    return {
      email: '',
      pass: '',
    };
  },
};
</script>
<style lang=""></style>
