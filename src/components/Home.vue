 <template>
  <div id="home">
  <head-app v-bind:title="title""></head-app>
    <img src="../assets/logo.png">
    <h2 >{{title}}</h2>
    <users v-bind:users="users"></users>
    <foot-app></foot-app>
  </div>
</template>
<script>
import users from './users';
import head from './header';
import foot from './footer';
export default {
  name: 'home',
  data(){
    return{
      title :  'home 组件',
       users : [
        {name:'henry',position:'dev',salary:'100',show:'false'},
        {name:'henry',position:'dev',salary:'100',show:'false'},
        {name:'henry',position:'dev',salary:'100',show:'false'},
        {name:'henry',position:'dev',salary:'100',show:'false'},
        {name:'henry',position:'dev',salary:'100',show:'false'},
        {name:'henry',position:'dev',salary:'100',show:'false'}
        ]
    }
  },
  methods :{
    updated(title){
      this.title=title;
    }
  },
  created: function(){
    this.$http.get('http://jsonplaceholder.typicode.com/users');
  },
  components : {
    "users" : users,
    "head-app":head,
    "foot-app":foot
  }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
