<template>
  <v-col>
    <page-header header="Websites" />
    <v-row class="mt-2">
      <template v-for="website in websites">
        <v-col cols="12" sm="6" :key="website.id">
          <website-card
            :websiteName="website.name"
            :websiteLink="website.url"
            :websiteImage="`https://picsum.photos/seed/${website.id}/100`"
          />
        </v-col>
      </template>
    </v-row>
  </v-col>
</template>

<script>
import PageHeader from '../components/PageHeader.vue'
import WebsiteCard from '../components/WebsiteCard.vue'
export default {
  components: { PageHeader, WebsiteCard },
  name: 'IndexPage',
  data() {
    return {
      websites: [
        {
          id: 1,
          name: 'Nyah McKenzie',
          url: 'http://medhurst.com/',
        },
        {
          id: 2,
          name: 'Ms. Marianna Schneider Sr.',
          url: 'http://stracke.com/adipisci-sit-libero-facilis-impedit-nobis.html',
        },
        {
          id: 3,
          name: 'Wyatt Corkery',
          url: 'http://breitenberg.net/',
        },
        {
          id: 4,
          name: 'Dr. Hailee Cassin I',
          url: 'http://www.oreilly.biz/ut-voluptas-esse-iure.html',
        },
        {
          id: 5,
          name: 'Miss Ophelia Bartell',
          url: 'http://bednar.com/cumque-voluptates-autem-soluta-aut.html',
        },
        {
          id: 6,
          name: 'Sandy Gleason',
          url: 'http://www.lind.com/alias-harum-est-harum.html',
        },
        {
          id: 7,
          name: 'Miss Tamara Fay',
          url: 'http://beier.com/',
        },
        {
          id: 8,
          name: 'Mr. Damian Spinka V',
          url: 'http://hettinger.com/accusamus-eos-eligendi-nihil-suscipit-quam-voluptatum',
        },
        {
          id: 9,
          name: 'Dashawn Schultz',
          url: 'http://dietrich.info/nemo-voluptas-eos-cumque-est-quisquam-sapiente',
        },
        {
          id: 10,
          name: 'Amely Blick',
          url: 'http://grant.com/deleniti-vel-nisi-ut-in.html',
        },
      ],
    }
  },
}
</script>
