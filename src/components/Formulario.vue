<template>
  <div>
    <b-container class="bv-example-row">
      <b-row>
        <b-col></b-col>
        <b-col>
          <h2 style="font-family: 'Bangers', cursive;">Contacto</h2><br>
          <b-form @submit.stop.prevent="onSubmit" style="font-family: 'Hind', sans-serif;">
            <b-form-group id="example-input-group-1" label="Nombre" label-for="example-input-1">
              <b-form-input
                id="example-input-1"
                name="example-input-1"
                v-model="$v.form.name.$model"
                :state="validateState('name')"
                aria-describedby="input-1-live-feedback"
                placeholder="Ingrese su nombre"
              ></b-form-input>

              <b-form-invalid-feedback id="input-1-live-feedback">Minimo 5 caracteres.</b-form-invalid-feedback>
            </b-form-group>

            <b-form-group id="example-input-group-1" label="Email" label-for="example-input-1">
              <b-form-input
                id="example-input-1"
                name="example-input-1"
                v-model="$v.form.email.$model"
                :state="validateState('email')"
                aria-describedby="input-1-live-feedback"
                placeholder="Ingrese su Correo Electrónico"
              ></b-form-input>

              <b-form-invalid-feedback id="input-1-live-feedback">Minimo 3 caracteres</b-form-invalid-feedback>
            </b-form-group>

            <b-form-group id="example-input-group-1" label="Teléfono" label-for="example-input-1">
              <b-form-input
                id="example-input-1"
                name="example-input-1"
                v-model="$v.form.telefono.$model"
                :state="validateState('telefono')"
                aria-describedby="input-1-live-feedback"
                type="number"
                placeholder="Ingrese su Teléfono"
              ></b-form-input>

              <b-form-invalid-feedback id="input-1-live-feedback">Minimo 9 Números.</b-form-invalid-feedback>
            </b-form-group>

            <div>
              <b-form-group label="Género">
                <b-form-radio v-model="selected" name="some-radios" value="A">Masculino</b-form-radio>
                <b-form-radio v-model="selected" name="some-radios" value="B">Femenino</b-form-radio>
              </b-form-group>
            </div>

            <b-button type="submit" variant="success">Submit</b-button>
          </b-form>
        </b-col>
        <b-col></b-col>
      </b-row>
    </b-container>
    <hr>
  </div>
</template>

<style>
body {
  padding: 1rem;
}
</style>

<script>
import { validationMixin } from 'vuelidate'
import { required, minLength } from 'vuelidate/lib/validators'

export default {
  mixins: [validationMixin],
  data () {
    return {
      form: {
        name: null,
        email: null,
        telefono: null

      }
    }
  },
  validations: {
    form: {
      telefono: {
        required,
        minLength: minLength(9)
      },
      name: {
        required,
        minLength: minLength(5)
      },
      email: {
        required,
        minLength: minLength(3)
      }
    }
  },
  methods: {
    validateState (name, email, telefono) {
      const { $dirty, $error } = this.$v.form[name]
      return $dirty ? !$error : null
    },
    resetForm () {
      this.form = {
        name: null,
        telefono: null,
        email: null
      }

      this.$nextTick(() => {
        this.$v.$reset()
      })
    },
    onSubmit () {
      this.$v.form.$touch()
      if (this.$v.form.$anyError) {
        return
      }

      alert('Form submitted!')
    }
  }
}
</script>

<style scoped>
.bv-example-row{
  margin-top: 40px;
}
</style>
