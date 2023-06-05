<template>
  <div >
    <buttonRendering color="primary"/>
    <div v-if="type === 'A' ">
      A
    </div>
    <div v-else-if="type==='B' " >
      B
    </div>
    <div v-else-if="type==='C' " >
      C
    </div>
    <div v-else-if="type==='D' " >
      D
    </div>
    <div v-else>
      Not A/B/C
    </div>
    <h2 v-show="ok"> Hello Mony !</h2>

  </div>
</template>
<script>
  import buttonRendering from '../components/Button'
  export default {
    name: 'HomePage',
    components: {
      buttonRendering
    },
    data() {
    return {
      ok : true
    }
  },
  }
</script>
