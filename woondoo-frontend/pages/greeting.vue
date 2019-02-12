<template>
  <div>
    <Header /> 
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Header from '~/components/shared/Header'
import '~/assets/scss/greeting.scss'

export default {
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
