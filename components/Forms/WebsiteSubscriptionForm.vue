<template>
  <v-form ref="form" v-model="isFormValid" lazy-validation>
    <v-text-field
      v-model="subscriptionForm.email"
      :rules="emailRule"
      label="E-mail"
      required
      outlined
    ></v-text-field>

    <v-row justify="center" class="pt-5">
      <v-btn
        :disabled="!isFormValid"
        color="primary"
        @click="login"
        class="white--text rounded"
        :loading="isLoading"
        tile
      >
        Subscribe
      </v-btn>

      <v-btn
        @click="$refs.form.reset()"
        tile
        class="ml-2 rounded"
        dark
        color="error"
      >
        Reset
      </v-btn>
    </v-row>
  </v-form>
</template>

<script>
const emailRule = [
  (v) => !!v || 'E-mail is required',
  (v) =>
    (!!v &&
      /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/.test(
        v
      )) ||
    'Email must be valid',
]

export default {
  data() {
    return {
      subscriptionForm: {
        isFormValid: false,
        isLoading: false,
      },
    }
  },
  computed: {
    emailRule() {
      return emailRule
    },
  },
}
</script>
