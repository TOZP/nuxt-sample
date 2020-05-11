<template>
  <v-card
    class="mx-auto"
    tile
  >
    <v-list dense>
      <v-subheader>仕事カテゴリ</v-subheader>
      <v-list-item-group v-model="item" color="primary">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
          <v-list-item-icon>
            <v-icon>mdi-chevron-right</v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    item: 0,
    items: [
      { text: 'システム開発' },
      { text: 'アプリ・スマートフォン開発' },
      { text: 'ハードウェア設計・開発' },
      { text: 'ホームページ制作・Webデザイン' },
      { text: 'デザイン' },
      { text: 'ライティング・記事作成' },
      { text: 'ネーミング・アイデア' },
      { text: '翻訳・通訳サービス' },
      { text: 'ECサイト・ネットショップ構築' },
      { text: 'サイト運営・ビジネス' },
      { text: '事務・ビジネスサポート・調査' },
      { text: 'カンタン作業' },
      { text: '写真・画像・動画' },
      { text: '3D-CG制作' },
      { text: '音楽・音響・BGM' },
      { text: 'プロジェクト・保守運用メンバー募集' },
      { text: '暮らし・社会' }
    ],
  })
}
</script>
