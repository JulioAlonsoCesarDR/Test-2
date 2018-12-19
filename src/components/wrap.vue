<template>
  <div>
    <content-header/>
    <search/>
  </div>
</template>

<script>
import ContentHeader from './header'
import Search from './search'
export default {
  name: 'wrap',
  components: {
    ContentHeader,
    Search
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>