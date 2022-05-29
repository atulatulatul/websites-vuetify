<template>
  <v-dialog v-model="websiteFormDialog" width="500" class="rounded-xl">
    <template v-slot:activator="{ on, attrs }">
      <v-btn class="mx-2" fab x-small color="pink" v-bind="attrs" v-on="on">
        <v-icon color="white"> mdi-bell </v-icon>
      </v-btn>
    </template>

    <v-card class="rounded">
      <v-toolbar color="primary" class="title" dark elevation="0">
        Subscribe Website
        <v-spacer />
        <v-btn
          class="mx-2"
          fab
          x-small
          color="transparent"
          v-bind="attrs"
          v-on="on"
          elevation="0"
          @click="
            () => {
              websiteFormDialog = false
            }
          "
        >
          <v-icon color="white"> mdi-close </v-icon>
        </v-btn>
      </v-toolbar>
      <v-card-text class="py-8">
        <website-subscription-form />
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
import WebsiteSubscriptionForm from './Forms/WebsiteSubscriptionForm.vue'
export default {
  components: { WebsiteSubscriptionForm },
  data() {
    return {
      websiteFormDialog: false,
    }
  },
}
</script>
