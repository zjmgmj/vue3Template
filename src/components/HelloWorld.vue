<template lang="pug">
div
  span 2222{{count}}{{num}}
</template>

<script>
import {ref} from 'vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup(props) {
    const count = ref(1)
    console.log('----------setUp', props)
    return {count}
  },
  data() {
    return{
      num: 0
    }
  },
  mounted() {
    console.log('count', this.count++)
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
