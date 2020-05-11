<template>
  <v-layout column>
    <v-flex>
      <v-breadcrumbs
        class="pl-0"
        :items="items"
        divider="-"
      ></v-breadcrumbs>
    </v-flex>
    <v-flex>
      <work-search-result-title
        category="すべて"
        count="5"
      />
    </v-flex>
    <v-row>
      <v-col lg="3">
        <work-category />
      </v-col>
      <v-col lg="9">
        <work-list />
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
import WorkSearchResultTitle from '~/components/molecules/WorkSearchResultTitle.vue'
import WorkCategory from '~/components/molecules/WorkCategory.vue'
import WorkList from '~/components/organisms/WorkList.vue'
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    WorkSearchResultTitle,
    WorkCategory,
    WorkList
  },
  data () {
    return {
      items: [
        {
          text: 'TOPページ',
          to: '/'
        },
        {
          text: '仕事を探す',
          disabled: true
        }
      ]
    }
  }
}
</script>
