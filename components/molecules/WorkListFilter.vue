<template>
  <v-row>
    <v-col lg="3" class="py-0">
      <v-select
        :items="items"
        v-model="value"
        solo
      ></v-select>
    </v-col>
    <v-col lg="3" class="py-0">
      <v-checkbox v-model="check1" label="募集終了を隠す"></v-checkbox>
    </v-col>
    <v-col lg="3" class="py-0">
      <v-checkbox v-model="check2" label="詳細を表示する"></v-checkbox>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { text: '表示順を選択', value: null },
        { text: '新着', value: '1' },
        { text: '人気', value: '2' },
        { text: '金額が高い', value: '3' },
        { text: '応募期限が近い', value: '4' },
        { text: '応募が少ない', value: '5' }
      ],
      value: null,
      check1: false,
      check2: false
    }
  }
}
</script>
