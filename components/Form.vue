<template>
  <div>
    <section class="py-5 my-section">
      <b-container fluid class="mb-5">
        <b-row>
          <b-col>
            <h2 class="text-center text-light mb-4" style="font-size: 48px;">Test Form</h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <b-embed type="iframe" aspect="16by9" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3960.7047122522176!2d107.58782811407994!3d-6.925857094995903!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e68e6002ca1a6c5%3A0xbbb1518487a1823c!2sJl.%20Terusan%20Pasirkoja%2C%20Babakan%20Tarogong%2C%20Kec.%20Bojongloa%20Kaler%2C%20Kota%20Bandung%2C%20Jawa%20Barat!5e0!3m2!1sid!2sid!4v1597425847874!5m2!1sid!2sid&output=embed" width="1110" height="555" frameborder="0" style="border: 0; margin-bottom: 0;" allowfullscreen="" aria-hidden="false" tabindex="0"></b-embed>
          </b-col>
          <b-col>
            <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="text-light">
              <b-form-group id="input-group-1" label="Your Name:" label-for="input-1">
                <b-form-input id="input-1" v-model="form.name" required placeholder="Enter name"></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-2" label="Email address:" label-for="input-2" description="We'll never share your email with anyone else.">
                <b-form-input id="input-2" v-model="form.email" type="email" required placeholder="Enter email"></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-3" label="Password:" label-for="input-3">
                <b-form-input id="text-password" type="password" v-model="form.password" required placeholder="Enter Password" aria-describedby="password-help-block"></b-form-input>
                <b-form-text id="password-help-block">
                  Your password must be 8-20 characters long, contain letters and numbers, and must not
                  contain spaces, special characters, or emoji.
                </b-form-text>
              </b-form-group>

              <b-form-group id="input-group-4" label="Food:" label-for="input-4">
                <b-form-select id="input-4" v-model="form.food" :options="foods" required></b-form-select>
              </b-form-group>

              <b-form-group id="input-group-5">
                <b-form-checkbox-group v-model="form.checked" id="checkboxes-5">
                  <b-form-checkbox value="me">Check me out</b-form-checkbox>
                  <b-form-checkbox value="that">Check that out</b-form-checkbox>
                </b-form-checkbox-group>
              </b-form-group>

              <b-button type="submit" variant="primary">Submit</b-button>
              <b-button type="reset" variant="danger">Reset</b-button>
            </b-form>
            <!-- <b-card class="mt-3" header="Form Data Result">
              <pre class="m-0">{{ form }}</pre>
            </b-card> -->
          </b-col>
        </b-row>
      </b-container>
    </section>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          name: '',
          email: '',
          password: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.name = ''
        this.form.email = ''
        this.form.password = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    },
    computed: {
      validation() {
        return this.password.length > 7 && this.password.length < 21
      }
    }
  }
</script>

<style>
  .my-section {
    background: linear-gradient(90deg, #30A4FB, #44E4C5);
  }
</style>
