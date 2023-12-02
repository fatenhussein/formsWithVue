<template lang="">
  <form @submit.prevent="handlesubmit">
    <label> Email:</label>
    <input type="email"  v-model="email" />

    <label> Password:</label>
    <input type="password"  v-model="pass" />

    <label>Role:</label>

    <select v-model="role">
      <option value="developer">web developer</option>
      <option value="designer">web designer</option>
    </select>

    <label> skills:::</label>
    <input type="text" v-model="tempSkill" @keyup.alt="addSkill" />

    <div class="terms">
      <input type="checkbox" v-model="terms" />

      <label> accept terms and conditions </label>
    </div>

    <div>
      <input type="checkbox" value="shone" v-model="names" />
      <label>shone</label>
    </div>
    <div>
      <input type="checkbox" value="ftft" v-model="names" />
      <label>ftft</label>
    </div>
    <div>
      <input type="checkbox" value="faten" v-model="names" />
      <label>faten</label>
    </div>

    <button type="submit">submit</button>
  </form>

  <p>email:{{ email }}</p>
  <p>pass:{{ pass }}</p>
  <p>role:{{ role }}</p>

  <p>terms accsepted :{{ terms }}</p>

  <p>{{ names }}</p>

  <div v-for="skill in skills" :key="skill">
    <span @click="deleteSkill(skill)">{{ skill }}</span>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: 'hhh',
      pass: '',
      role: 'designer',
      terms: false,
      names: [],
      tempSkill: '',
      skills: [],
    };
  },

  methods: {
    addSkill(e) {
      console.log(e);
      if (e.key === ',' && this.tempSkill) {
        if (!this.skills.includes(this.tempSkill)) {
          this.skills.push(this.tempSkill);
        }

        this.tempSkill = '';
      }
    },
    deleteSkill(skill) {
    this.skills = this.skills.filter((item) => {
      return skill !== item;
    });
  },
  handlesubmit(){
console.log("form submited")
  }
  },

};
</script>
<style lang=""></style>
