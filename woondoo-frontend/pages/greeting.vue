<template>
  <div>
    <Header /> 
    <p>
    </p>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Header from '../components/shared/Header'

export default {
  head: {
    link: [
      { rel: 'stylesheet', href: '/css/greeting.css' }
    ]
  },
  fetch({ store }) {
  },
  computed: mapState([
    'counter'
  ]),
  methods: {
  },
  components: {
    Header
  }
}
</script>
