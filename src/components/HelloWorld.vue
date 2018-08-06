<template>
  <div class="hello">
    <h1>{{$t('message.title')}}</h1>
    <p>{{$t('message.i1')}}</p>
    <el-button type="success" @click="switchLang">{{$t('message.btn')}}</el-button>
    <user class="user"></user>
  </div>
</template>

<script>
import User from './User'
export default {
  name: 'HelloWorld',
  components:{
    User
  },
  data () {
    return {
      lang: this.$i18n.locale==='en'?'cn':'en',
      //message:this.$i18n.message
    }
  },
  mounted(){
    //console.log(this.$i18n)
  },
  methods:{
    switchLang()  {
        this.$i18n.locale = this.$i18n.locale==='en'?'cn':'en' 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.user{
  margin-top: 20px
}
</style>
