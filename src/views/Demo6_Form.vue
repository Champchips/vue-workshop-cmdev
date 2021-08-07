<template>
  <div id="Demo6">
    <h1>Demo6 : Form</h1>
    <form @submit.prevent="submit">
      <!-- firstname -->
      <div :class="formgroups">
        <label for="first_name">FirstName : </label>
        <input
          type="text"
          name="first_name"
          v-model.trim="applicant.first_name"
        />
      </div>

      <!-- lastname -->
      <div :class="formgroups">
        <label for="first_name">LastName : </label>
        <input
          type="text"
          name="last_name"
          v-model.trim="applicant.last_name"
        />
      </div>

      <!-- sex -->
      <div :class="formgroups">
        <lable for="sex">Male : </lable>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />

        <lable for="sex">Female : </lable>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>

      <!-- age -->
      <div :class="formgroups">
        <label for="age">Age : </label>
        <input type="number" v-model.number="applicant.age" />
      </div>

      <!-- courses -->
      <div :class="formgroups">
        <select name="courses" v-model="applicant.courses">
          <option value="react">React</option>
          <option value="angular">Angular</option>
          <option value="vuejs">Vue</option>
        </select>
      </div>
      <button style="margin: 5px; margin-right:" type="button" @click.exact="clear" @click.alt="useDefault">
        Clear
      </button>
      <button style="margin: 5px;" type="submit">Submit</button>
    </form>
    <div style="margin-top: 16px; color:red;">
      #Spy {{ JSON.stringify(applicant) }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        age: 0,
        courses: "react",
      },
      formgroups: "formDiv",
    };
  },
  methods: {
    submit() {
      //   event.preventDefault();
      alert(JSON.stringify(this.applicant));
    },
    clear() {
      this.applicant = {
        first_name: "",
        last_name: "",
        sex: "male",
        courses: "react",
        age: 0,
      };
    },
    useDefault() {
      this.applicant = {
        first_name: "UNKNOWN",
        last_name: "UNKNOWN",
        sex: "male",
        courses: "react",
        age: 0,
      };
    },
  },
};
</script>

<style>
.formDiv {
  margin-bottom: 10px;
}
</style>
