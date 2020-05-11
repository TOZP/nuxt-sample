<template>
  <div class="my-8 d-flex justify-start align-center">
    <h1 class="category">
      {{category}}
      <span>の仕事情報を探す</span>
    </h1>
    <div class="count">{{count}}件のうち、{{start}}〜{{end}}件を表示</div>
  </div>
</template>

<script>
export default {
  props: {
    category: {
      type: String,
      required: true
    },
    count: {
      type: String,
      required: true
    }
  },
  data () {
    return {}
  },
  computed: {
    start () {
      return '1'
    },
    end () {
      return Number(this.count) > 50 ? '50' : this.count
    }
  }
}
</script>

<style scoped>
.category {
  font-size: 25px;
}
.category span {
  font-size: 18px;
}
.count {
  margin-left: 10px;
  color: gray;
}
</style>
