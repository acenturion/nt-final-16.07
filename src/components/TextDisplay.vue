<template>
  <div>
    <h4>{{formatString}}</h4>
  </div>
</template>

<script>
export default {
  name: 'TextDisplay',
  props: {
    message: String
  },
  data(){
    return{
    }
  },
  computed:{
    formatString(){
      let result = '';
      let letter = this.message.split('').map(x => {
        switch (x) {
          case 'a': return 'u';
          case 'e': return 'o';
          case 'o': return 'e';
          case 'u': return 'a';
          default: return x;
        }
      })

      for (let i = 0 ;i < letter.length; i++){
        result += letter[i];
      }

      return result.toUpperCase();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
