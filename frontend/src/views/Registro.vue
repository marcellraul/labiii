<template>
  <v-app id="inspire">
    <v-main>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="10" md="8">
            <v-card class="elevation-3">
              <v-toolbar color="#145A32" dark flat>
                <v-toolbar-title>Registro</v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-card-text>
                <form>
                  <v-text-field
                    color="#145A32"
                    v-model="name"
                    :error-messages="nameErrors"
                    :counter="15"
                    label="Name"
                    required
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                  ></v-text-field>

                  <v-text-field
                    color="#145A32"
                    v-model="password"
                    :append-icon=" 'mdi-eye-off'"
                    :type=" 'password'"
                    name="input-10-1"
                    label="Password"
                    hint="At least 6 characters"
                    counter
                  ></v-text-field>

                  <v-text-field
                    color="#145A32"
                    v-model="email"
                    :error-messages="emailErrors"
                    label="E-mail"
                    required
                    @input="$v.email.$touch()"
                    @blur="$v.email.$touch()"
                  ></v-text-field>
                  <v-select
                    color="#145A32"
                    v-model="select"
                    :items="items"
                    :error-messages="selectErrors"
                    label="Tipo"
                    required
                    @change="$v.select.$touch()"
                    @blur="$v.select.$touch()"
                  ></v-select>
                  <v-checkbox
                    v-model="checkbox"
                    :error-messages="checkboxErrors"
                    label="Do you agree?"
                    required
                    @change="$v.checkbox.$touch()"
                    @blur="$v.checkbox.$touch()"
                  ></v-checkbox>

                  <v-btn class="mr-4" color="#145A32" @click="AddRegistro" type="submit">Resgistrar</v-btn>
                  <v-btn @click="clear">clear</v-btn>
                </form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(15) },
    email: { required, email },
    select: { required },
    password: { required },
    checkbox: {
      checked(val) {
        return val;
      }
    }
  },

  data: () => ({
    name: "",
    email: "",
    password: "",
    select: null,
    items: ["Persona", "Empresa"],
    checkbox: false
  }),

  computed: {
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      return errors;
    },
    selectErrors() {
      const errors = [];
      if (!this.$v.select.$dirty) return errors;
      !this.$v.select.required && errors.push("Item is required");
      return errors;
    },
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 15 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    }
  },

  methods: {
    AddRegistro() {
      const user = {
        name: this.name,
        email: this.email,
        password: this.password,
        tipo: this.select
      };
      console.log(user);
      const resp = this.$store.dispatch("users/create", user);
      console.log(resp);
    },

    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.password = "";
      this.select = null;
      this.checkbox = false;
    }
  },
  mounted() {
    console.log("mounted is working");
  },

  created() {
    this.$store.dispatch("users/gets"); //nombre del modulo y nombre del actions
    //this.$store.dispatch("tipop/gets");
    this.$store.dispatch("tipop/gets");
  }
};
</script>
