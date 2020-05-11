<template>
  <v-card class="mb-4">
    <div class="test">
      <v-row>
        <v-col class="pb-0">
          <v-chip
            small
            color="red"
            label
            text-color="white"
            class="chip-text"
          >PR
          </v-chip>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="6">
          <div class="title-work-detail">{{work.title}}</div>
          <div class="subtitle-work-detail">
            <v-icon small color="#1867c0">mdi-folder</v-icon>
            {{work.category}}
          </div>
        </v-col>
        <v-col cols="2">{{work.price}}</v-col>
        <v-col cols="2">契約数 {{work.contractors}} 人</v-col>
        <v-col cols="2">あと {{work.deadlineDays}} 日</v-col>
      </v-row>
      <v-row>
        <v-col cols="6">
          <v-avatar
            size="36px"
          >
            <img
              alt="Avatar"
              src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460"
            >
          </v-avatar>
          <span class="ml-2">John Leider</span>
        </v-col>
        <v-col cols="6">
          <div class="float-right">
            <span class="publication-date">掲載日：{{work.publicationDate}}</span>
            <v-btn class="ml-3" depressed small outlined>
              <v-icon color="yellow" left>mdi-star</v-icon>気になる
            </v-btn>
            <v-btn color="success" class="ml-3" depressed small>詳細を見る</v-btn>
          </div>
        </v-col>
      </v-row>
    </div>
  </v-card>
</template>

<script>
export default {
  props: {
    work: {
      type: Object,
      required: true
    }
  },
  data () {
    return {}
  }
}
</script>

<style scoped>
.test {
  padding-left: 12px;
  padding-right: 12px;
}
.chip-text {
  font-weight: bold;
}
.title-work-detail {
  font-size: 14px;
  margin-bottom: 8px;
  color: #1867c0;
  font-weight: bold;
}
.subtitle-work-detail {
  font-size: 12px;
  color: #1867c0;
}
.publication-date {
  font-size: 12px;
  color: gray;
}
</style>
