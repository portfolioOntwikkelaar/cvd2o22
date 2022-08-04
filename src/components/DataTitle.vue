<template>
  <div class="text-center">
  <h2 class="text=3xl font-bold">{{text}}
    <div class="text-2xl mt-4 mb-10" >
    {{timestamp}}</div>
  </h2>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  name: 'DataTitle',
  props: ['text', 'dataDate'],
  computed: {
    timestamp: function() {
      return moment(this.dataDate).format('MMMM Do YYYY, h:mm:ss a')
    },
  },
}
</script>