<template>
  <v-hover v-slot="{ hover }">
    <v-card :elevation="hover ? 2 : 0" class="rounded-xl">
      <v-sheet class="d-flex justify-space-between">
        <v-sheet class="d-flex text-truncate text-no-wrap">
          <v-sheet>
            <v-img
              height="80"
              width="80"
              max-height="80"
              max-width="80"
              :src="websiteImage"
              class="rounded-xl"
            ></v-img>
          </v-sheet>

          <v-sheet
            class="d-flex align-self-center ml-2 text-truncate text-no-wrap"
          >
            <v-sheet class="text-truncate text-no-wrap pr-2">
              <div class="text-h6 grey--text text--darken-2">
                {{ websiteName }}
              </div>
              <a
                :href="websiteLink"
                class="text-truncate text-no-wrap text-decoration-none"
                >{{ websiteLink }}</a
              >
            </v-sheet>
          </v-sheet>
        </v-sheet>

        <v-sheet class="d-flex align-self-center justify-end">
          <subscribe-button />
        </v-sheet>
      </v-sheet>
    </v-card>
  </v-hover>
</template>
<script>
import SubscribeButton from './SubscribeButton.vue'
export default {
  components: { SubscribeButton },
  props: {
    websiteName: {
      type: String,
      required: true,
    },
    websiteLink: {
      type: String,
      required: true,
    },
    websiteImage: {
      type: String,
      requried: true,
    },
  },
}
</script>
