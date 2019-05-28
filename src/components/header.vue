 <template>
  <div id="header">
  <h2 v-on:click="changed">{{title}}</h2>
    <ul>
      <li  v-for="nav in navs" >{{nav}}</li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'header',
  props:{
      title : {
          type:String
      }
  },
  data(){
    return{
      navs : ['商城','女装','男装','儿童装'],
    }
  },
  methods : {
      changed(){
      this.$emit("changedTitle",'子向父传值');
      }
  }
}
</script>
<style  scoped>
#header ul {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
  height:100px;
  background:green;
  display:flex;
  flex-flow:row wrap;
  justify-content:center;
  align-items: center;
}
li{
flex-grow:1;


  
}
</style>
