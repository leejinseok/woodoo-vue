<template>
  <div class="indexPage">
    <Header isWhite="true"/>
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

<style lang="scss" scoped>
$asideBackImg: '/images/main_03.jpg';

.aside-top {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  position: relative;
  background-image: url($asideBackImg);
  background-position: center center;
  background-size: cover;
  padding-top: 80px;
  box-sizing: border-box;
}

.aside-top::after {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .35);
  z-index: 0;
}

.aside-top img {
  position: absolute;
  left: 50%;
  top: -100px;
  max-width: 100%;
  transform: translateX(-50%);
  z-index: 0;
}

.aside-top .aside-top__inner {
  position: relative;
  z-index: 1;
} 

.aside-top .aside-top__inner .describe {
  color: #fff;
  font-size: 16px;
  font-weight: normal;
  line-height: 1.3;
  font-size: 38px;
  margin-top: 50px;
}

.aside-top .aside-top__inner .container {
  margin-top: 50px;
}

.aside-top .aside-top__inner .container .card {
  background-color: #fff;
  border-radius: 6px;
  width: 100%;
  height: 300px;;
}
</style>
