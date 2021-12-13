<template>
  <div>
    <Header />
    <main id="main">
      <section id="youtubeCont">
        <div class="container">
          <WrapTitle name1="news" name2="reference" />
          <div v-for="user in users" :key="user.id">
            <p>{{ user.title }}</p>
            <p>{{ user.time }}</p>
          </div>
        </div>
      </section>
      <ContInfo />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import WrapTitle from '@/components/WrapTitle.vue'
import ContInfo from '@/components/ContInfo.vue'
import axios from 'axios'

export default {
  components: {
    Header,
    Footer,
    WrapTitle,
    ContInfo,
  },
  data() {
    return {
      users: [],
    }
  },

  created() {
    var vm = this
    axios
      .get('https://api.hnpwa.com/v0/news/1.json')
      .then(function (res) {
        console.log(res)
        vm.users = res.data
      })
      .catch(function (err) {
        console.log(err)
      })
  },
}
</script>

<style lang="scss">
#youtubeCont {
  background-color: #000;
  color: #fff;
  padding-bottom: 400px;
  font-family: 'SCoreDream';
}
.youtube__cont {
  color: #fff;

  h2 {
    border-bottom: 1px solid #fff;
    margin-bottom: 40px;
  }
  .youtube {
    display: flex;
    align-content: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;

    > div {
      flex: 0 0 24%;
      margin-bottom: 2%;

      .title {
        margin: 10px 0;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
      }
    }
  }
  .search {
    display: flex;
    justify-content: space-between;
    margin-bottom: 50px;

    input {
      flex: 0 0 79%;
      background: transparent;
      border: 0;
      color: #fff;
      border: 1px solid #fff;
      font-family: 'SCoreDream';
      padding: 5px 10px;
      outline: #fff;

      &::placeholder {
        color: #fff;
      }
    }
    button {
      flex: 0 0 20%;
      border: 0;
      font-family: 'SCoreDream';
      background: #fff;
      padding: 10px;
    }
  }
}
</style>
