<template>
  <div>
    <v-row>
      <v-col class="py-0">
        <work-search-box />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="py-0">
        <work-list-filter />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="py-0">
        <work-list-detail
          v-for="work in works"
          :key="`key_work_${work.id}`"
          :work="work"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import WorkSearchBox from '~/components/molecules/WorkSearchBox.vue'
import WorkListFilter from '~/components/molecules/WorkListFilter.vue'
import WorkListDetail from '~/components/molecules/WorkListDetail.vue'

export default {
  components: {
    WorkSearchBox,
    WorkListFilter,
    WorkListDetail
  },
  data () {
    return {
      works: [
        {
          id: '1',
          title: '「商品感想モニター」 300円から1000円前後　継続もあり！',
          category: 'その他（カンタン作業）',
          text: '',
          price: '10,000円 〜 50,000円',
          contractors: 1,
          deadlineDays: 8,
          publicationDate: '2020/05/10'
        },
        {
          id: '2',
          title: '■まずはお試し1記事からOK■『風俗で遊んだ体験談』記事の執筆をお願いします。報酬UP制度あり！長期継続歓迎！',
          category: 'ブログ記事作成（その他）',
          text: '',
          price: '10,000円 〜 50,000円',
          contractors: 2,
          deadlineDays: 7,
          publicationDate: '2020/05/09'
        },
        {
          id: '3',
          title: '競技用ストップウォッチ・映像記録プログラムの設計・製作',
          category: '回路設計・組み込みソフト開発',
          text: '',
          price: '700円 / 件',
          contractors: 3,
          deadlineDays: 6,
          publicationDate: '2020/05/08'
        },
        {
          id: '4',
          title: '【英会話スクールに通っている主婦の方】未経験からワードプレスとライティング、英語も習得★学びが多い仕事★初心者',
          category: 'ブログ記事作成（ビジネス）',
          text: '',
          price: '2,500円',
          contractors: 4,
          deadlineDays: 5,
          publicationDate: '2020/05/07'
        },
        {
          id: '5',
          title: 'モゴモゴバスターをやったことがある方｜ゼロからライティングを学んでライターとしてやっていきたい方・ワードプレス',
          category: 'ブログ記事作成（ビジネス）',
          text: '',
          price: '予算はメンバーと相談',
          contractors: 5,
          deadlineDays: 4,
          publicationDate: '2020/05/06'
        }
      ]
    }
  }
}
</script>
