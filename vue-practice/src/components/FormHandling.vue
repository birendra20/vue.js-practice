<template>
  <hr />
  <div>
    <pre>
        {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>
    <div>
      <label for="profile">profile summary</label>
      <textarea id="profile" v-model="formValues.profileSummary" />
    </div>
    <div>
      <label for="country">country</label>
      <select id="country" v-model="formValues.country">
        <option value="">select a country</option>
        <option value="india">India</option>
        <option value="vietnam">vietnam</option>
        <option value="singapore">singapore</option>
      </select>
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="india">India</option>
        <option value="vietnam">vietnam</option>
        <option value="singapore">singapore</option>
      </select>
    </div>
    <hr />
    <div>
      <!-- <input type="checkbox" v-model="formValues.remoteWork" /> -->
      <input
        type="checkbox"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
      <label for="remoteWork">open to remote work?</label>
    </div>
    <div>
      <label>Skill set</label>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input type="checkbox" id="js" value="js" v-model="formValues.skillSet" />
      <label for="js">Js</label>
    </div>
    <hr />
    <div>
      <p>Years of Experience</p>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.yearsOfExperience"
      />
      <label for="0-2">0-2</label>
      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.yearsOfExperience"
      />
      <label for="3-5">3-5</label>
      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.yearsOfExperience"
      />
      <label for="6-10">6-10</label>
    </div>
    <div>
      <button>Submit</button>
    </div>
  </form>
  <hr />
</template>

<script>
export default {
  name: "FormHandling",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        //remoteWork: false,
        remoteWork: "no",
        skillSet: [],
        yearsOfExperience: "",
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log("form values", this.formValues);
      alert(JSON.stringify(this.formValues));
    },
  },
};
</script>

<style scoped>
label {
  font-weight: bold;
  display: inline-flex;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.4;
  color: black;
  background-color: white;
  background-image: none;
}
</style>
