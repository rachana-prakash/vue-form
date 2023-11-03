<template>
  <div>
    <form @submit.prevent="submitForm">
      <div class="form-control">
        <input
          type="text"
          id="firstName"
          placeholder="First Name"
          v-model.trim.lazy="formValues.firstName"
        />
      </div>
      <div class="form-control">
        <input
          type="text"
          id="lastName"
          placeholder="Last Name"
          v-model.trim.lazy="formValues.lastName"
        />
      </div>
      <div class="form-control">
        <input
          type="text"
          id="email"
          placeholder="Work Email"
          v-model.trim.lazy="formValues.workEmail"
        />
      </div>
      <div class="form-control">
        <input
          type="text"
          id="email"
          placeholder="Company Name"
          v-model.trim.lazy="formValues.companyName"
        />
      </div>
      <div class="form-control">
        <select id="companySize" v-model="formValues.companySize">
          <option value="" disabled selected class="title">Company Size</option>
          <option value="small">less than 100</option>
          <option value="medium">between 100 - 1000</option>
          <option value="large">more than 1000</option>
        </select>
      </div>
      <div class="form-control">
        <input
          type="text"
          id="phone"
          placeholder="Phone"
          v-model.trim.lazy="formValues.phone"
        />
      </div>

      <div class="form-control">
        <select id="country" v-model="formValues.country">
          <option value="" selected>United States</option>
          <option value="india">India</option>
          <option value="singapore">Singapore</option>
        </select>
      </div>

      <button class="submit-btn">Continue</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "RegistrationForm",
  data() {
    return {
      formValues: {
        firstName: "",
        lastName: "",
        workEmail: "",
        companyName: "",
        companySize: "",
        phone: "",
        country: "",
      },
    };
  },
  methods: {
    submitForm() {
      console.log(this.formValues);
    },
  },
};
</script>

<style scoped>
input[type="text"],
select {
  display: block;
  width: 100%;
  height: 52px;
  padding: 0 12px;
  font-size: 14px;
  line-height: 1.4;
  color: white;
  background-color: var(--blue1);
  background-image: none;
  border: none;
  border-bottom: 1px solid rgba(255, 255, 255, 0.25);
  border-radius: 4px;
}
input::placeholder {
  color: rgba(255, 255, 255, 0.55);
}

.form-control {
  margin-bottom: 10px;
  display: flex;
  padding: 5px 15px;
}
form {
  background-color: var(--blue1);
  padding: 10px;
  border-radius: 15px;
}
.submit-btn {
  height: 48px;
  background: white;
  color: var(--blue1);
  border: none;
  width: 150px;
  font-size: 16px;
  border-radius: 35px;
  margin: 5px 15px;
}
@media screen and (min-width: 768px) {
  input[type="text"],
  select {
    font-size: 16px;
  }
  .form-control {
    margin-bottom: 20px;
    padding: 15px;
  }
  .submit-btn {
    height: 48px;
    width: 180px;
    font-size: 18px;
  }
}
</style>
