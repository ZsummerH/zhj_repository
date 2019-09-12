<template>
  <div class="hellow">
    <el-carousel indicator-position="outside">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3>{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
    <ul>
       <router-link to="/home">吃货点击</router-link>
       <router-link to="/myComponet">自定义组件</router-link>
    </ul>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'flextest'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
  text-align: left;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.hello{
  display: flex;
  flex-direction: column;
}

#flexTest  {
  display: flex; /*使用flex布局*/
  flex-direction: column;
  width: 200px;
  text-align: left;
}


input  {
  flex-grow: 0; /*0:使用本身宽度,不拉伸,1:宽度拉伸,占用剩余宽度*/
  align-self: stretch;/*居中高度不拉伸,flex-start：顶边对齐，高度不拉伸;
            flex-end：底边对齐，高度不拉伸;stretch：默认值，高度自动拉伸*/

}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(4n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(4n+1) {
  background-color: #d3dce6;
}

.el-carousel__item:nth-child(4n+2) {
  background-color: bisque;
}

.el-carousel__item:nth-child(4n+3) {
  background-color: lightyellow;
}
</style>
