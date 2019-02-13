<template>
  <div>
    <Header :isWhite="isWhite"/>
    <aside class="aside-top">
      <div class="aside-top__inner full-width">
        <h3 class="describe">
          희년을 누리는 교회, <br>
          운두교회에 오신 여러분을 환영합니다.
        </h3>
      </div>
    </aside>
  </div>
</template>

<script>
import axios from 'axios'
import { mapState } from 'vuex'
import Header from '~/components/shared/Header'
import Notice from '~/components/index/Notice/Notice'

export default {
  data () {
    return {
      isWhite: true
    }
  },
  asyncData (context) {
    return axios.get(`https://jsonplaceholder.typicode.com/posts`)
    .then((res) => {
      return { 
        notices: res.data.slice(0, 10)
      }
    })
  },
  fetch({ store, params }) {
    store.commit('increment')
  },
  computed: mapState([
    'counter'
  ]),
  methods: {
    increment () {
      this.$store.commit('increment')
    },
  },
  created: function () {
    console.log(this);
  },
  components: {
    Header,
    Notice
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

</style>
