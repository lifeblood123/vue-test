 <template>
  <div id="users">
    <ul>
      <li v-for="user in users" v-on:click="user.show=!user.show">
        <h2>{{user.name}}</h2>
        <h3>{{user.position}}</h3>
        <h4 v-show="!user.show">{{user.salary}}</h4>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'users',
  props:{
    users:{
      type:Array,
      required:'true'
    }
  },
  data(){
    return{
     
    }

  }
}
</script>

<style  scoped>
#users {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
li{
  flex-grow:1;
  border:1px solid #ccc;
  list-style:none;
  text-decoration:none;
}
ul{
  display:flex;

  flex-wrap:wrap;
  flex-direction:row;
  justify-content:center;
    align-items: center;


}
</style>
