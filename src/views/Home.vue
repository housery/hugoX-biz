<template>
  <div class="home">
    <el-container>
      <el-header>
        <Header></Header>
      </el-header>

      <el-container>
        <el-aside width="300px">
          <Aside></Aside>
        </el-aside>

        <el-main>
          main
        </el-main>
      </el-container>
      <el-footer>
        <Footer></Footer>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Aside from '@/components/Aside.vue'

export default {
  name: 'home',
  components: {
    Header,
    Footer,
    Aside
  },
  data(){
    return {

    }
  }
}
</script>

<style scoped>
.el-aside{
  padding: 20px;
}
</style>
