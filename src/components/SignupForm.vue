<template lang="">
  <form>
    <label> Email:</label>
    <input type="email" required v-model="email" />

    <label> Password:</label>
    <input type="password" required v-model="pass" />

    <label>Role:</label>

    <select v-model="role">
      <option value="developer">web developer</option>
      <option value="designer">web designer</option>
    </select>




    <div class="terms">
        <input type="checkbox" v-model='terms'>

        <label > accept terms and conditions </label>

    </div>
  </form>

  <p>email:{{ email }}</p>
  <p>pass:{{ pass }}</p>
  <p>role:{{ role }}</p>

  <p>terms accsepted :{{terms}}</p>
</template>
<script>
export default {
  data() {
    return {
      email: 'hhh',
      pass: '',
      role: 'designer',
      terms: false
    };
  },
};
</script>
<style lang=""></style>
