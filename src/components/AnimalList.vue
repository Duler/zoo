<template>
  <div :id="msg"  >
    
  </div>
</template>

<script>
import moment from 'moment'

export default {
  data() {
    return {
      name: 'AnimalList',
      props: {
      msg: "Zoo"
      }
    }
  },
  methods: {
      
    },
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
