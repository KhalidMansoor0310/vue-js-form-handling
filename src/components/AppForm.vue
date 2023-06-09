<template>
  <div class="hello">
    <small>{{ JSON.stringify(formValues, null, 2) }}</small>
    <div class="container">
      <div class="row">
        <div class="col-md-6 m-auto">
          <form @submit.prevent="handleSubmit">
            <div class="form-group">
              <input
                type="text"
                placeholder="Enter your name"
                class="form-control"
                v-model="formValues.name"
              />
            </div>
            <div class="form-group my-3">
              <textarea
                type="text"
                placeholder="Enter your profile summary"
                class="form-control"
                v-model="formValues.profileSummary"
              >
              </textarea>
            </div>
            <div class="form-group my-3">
              <select
                type="text"
                placeholder="Select Country"
                class="form-control"
                v-model="formValues.country"
              >
                <option value="">Select Country</option>
                <option value="Pakistan">Pakistan</option>
                <option value="India">India</option>
                <option value="Canada">Canada</option>
              </select>
            </div>
            <div class="form-group my-3">
              <select
                type="text"
                placeholder="Select Job Location"
                class="form-control"
                multiple
                v-model="formValues.jobLocation"
              >
                <option value="">Select Job Location</option>
                <option value="Pakistan">Pakistan</option>
                <option value="India">India</option>
                <option value="Canada">Canada</option>
              </select>
            </div>
            <div class="form-group d-flex justify-content-start">
              <input
                type="checkbox"
                class="mx-2"
                v-model="formValues.remoteWork"
              />
              <label for="">Open to Remote Work ?</label>
            </div>
            <hr />
            <div class="form-group d-flex justify-content-start mt-4">
              <div>
                <input
                  type="checkbox"
                  class="mx-2"
                  value="html"
                  v-model="formValues.skills"
                />
                <label for="">HTML</label>
              </div>
              <div>
                <input
                  type="checkbox"
                  class="mx-2"
                  value="css"
                  v-model="formValues.skills"
                />
                <label for="">CSS</label>
              </div>
              <div>
                <input
                  type="checkbox"
                  class="mx-2"
                  value="javascript"
                  v-model="formValues.skills"
                />
                <label for="">JS</label>
              </div>
            </div>
            <div class="form-group d-flex justify-content-start mt-4">
              <p>Years of Experience</p>
              <div>
                <input
                  type="radio"
                  class="mx-2"
                  value="0-2"
                  v-model="formValues.yearOfExperience"
                />
                <label for="">0-2</label>
              </div>
              <div>
                <input
                  type="radio"
                  class="mx-2"
                  value="2-4"
                  v-model="formValues.yearOfExperience"
                />
                <label for="">2-4</label>
              </div>
              <div>
                <input
                  type="radio"
                  class="mx-2"
                  value="4-6"
                  v-model="formValues.yearOfExperience"
                />
                <label for="">4-6</label>
              </div>
            </div>

            <button type="submit" class="btn btn-primary">Submit Form</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: false,
        skills: [],
        yearOfExperience: "",
      },
    };
  },
  methods: {
    handleSubmit(e) {
      e.preventDefault();
      console.log(this.formValues);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
