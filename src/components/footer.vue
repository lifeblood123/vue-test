 <template>
  <div id="footer">
  <p>{{footer}}</p>  
  </div>
</template>

<script>
export default {
  name: 'footer',
  data(){
    return{
      footer : '这是一个简单的footer,就是这么酷'
    }

  }
}
</script>

<style  scoped>
#footer p {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
