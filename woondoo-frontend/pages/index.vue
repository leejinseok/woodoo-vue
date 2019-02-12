<template>
  <div>
    <Header />
    <aside class="aside-top">
      <div class="aside-top__inner full-width">
        <h3 class="describe">
          희년을 누리는 교회, <br>
          운두교회에 오신 여러분을 환영합니다.
        </h3>

        <div class="container">
          <div class="col-4">
            <div class="card notice">
              <p>공지사항</p>
            </div>
          </div>
          <div class="col-4">
            <div class="card gallery">
              <p>갤러리</p>
            </div>
          </div>
          <div class="col-4">
            <div class="card gallery">
              <p></p>
            </div>
          </div>
        </div>
      </div>
    </aside>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Header from '~/components/shared/Header'
import '~/assets/scss/index.scss'

export default {
  head: {
  },
  fetch({ store }) {
    store.commit('increment')
  },
  computed: mapState([
    'counter'
  ]),
  methods: {
    increment() {
      this.$store.commit('increment')
    }
  },
  created: function () {
  },
  components: {
    Header
  }
}
</script>
