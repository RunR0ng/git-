<script>
  import Welcome from './Welcome.vue'
  export default{
    name:'login',
    components:{Welcome},
    mounted(){
      this.$request({
        method: 'get',
        url: '/login',
        data: {
          name: 'Fred'
        } 
      }).then((res)=>{
        console.log(res)
      })
    },
    methods:{
      goHome(){
        this.$router.push('/welcome')
      }
    }
  }
</script>

<template>
  <h1>登陆界面</h1>
  <el-button @click='goHome'>回首页</el-button>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
