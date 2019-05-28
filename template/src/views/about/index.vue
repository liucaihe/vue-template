<template>
  <div class="about">
    <h1 class="about-h1">
      欢迎回来
    </h1>
    <p>{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      // .env 文件定义的变量
      msg: process.env.VUE_APP_API_HOST
    }
  },
  created () {
    this.$storage.set('ssss', { name: 'liucaihe' }, new Date().getTime() + 3000)
    // this.$storage.each((v, k) => {
    //   console.log(k, '===', v)
    // })
    // console.log(this.$storage.get('author'))
  }
}
</script>

<style lang="stylus">
.about-h1
  font-size 60px
  text-align left
  padding-left 50px

.lang-ul-box
  padding 0 36px
  display flex

  li
    flex 1
    border 1PX solid rgba(206, 206, 206, 1)
    height 50px
    width 126px
    line-height 50px
    border-radius 20px
    box-sizing border-box
    font-size 26px
    font-weight 500
    color rgba(102, 102, 102, 1)

</style>
