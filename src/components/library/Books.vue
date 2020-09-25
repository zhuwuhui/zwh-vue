<template>
  <div>
    <el-row style="height: 840px;">
      <!--<search-bar></search-bar>-->
      <el-tooltip effect="dark" placement="right"
                  v-for="item in books"
                  :key="item.id">
        <p slot="content" style="font-size: 14px;margin-bottom: 6px;">{{item.title}}</p>
        <p slot="content" style="font-size: 13px;margin-bottom: 6px">
          <span>{{item.author}}</span> /
          <span>{{item.date}}</span> /
          <span>{{item.press}}</span>
        </p>
        <p slot="content" style="width: 300px" class="abstract">{{item.abs}}</p>
        <el-card style="width: 135px;margin-bottom: 20px;height: 233px;float: left;margin-right: 15px" class="book"
                 bodyStyle="padding:10px" shadow="hover">
          <div class="cover">
            <img :src="item.cover" alt="封面">
          </div>
          <div class="info">
            <div class="title">
              <a href="">{{item.title}}</a>
            </div>
          </div>
          <div class="author">{{item.author}}</div>
        </el-card>
      </el-tooltip>
    </el-row>
    <el-row>
      <el-pagination
        :current-page="1"
        :page-size="10"
        :total="20">
      </el-pagination>
    </el-row>
  </div>
</template>

<script>
  export default {
    name: 'Books',
    data () {
      return {
        books: [
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/niu.jpg',
            title: '牛明照',
            author: '猪无悔',
            date: '2020-09-25',
            press: '郑州联想渠道大牛',
            abs: '街头路灯'
          },
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/long.jpg',
            title: '孙孟龙',
            author: '猪无悔',
            date: '2020-09-25',
            press: '孙董',
            abs: '筑家易杰伦'
          },
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/qi.jpg',
            title: '刘成洋',
            author: '猪无悔',
            date: '2020-09-25',
            press: '小七',
            abs: '可乐七'
          },
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/bin.jpg',
            title: '王亚彬',
            author: '猪无悔',
            date: '2020-09-25',
            press: '彬狗',
            abs: '彬彬有礼'
          },
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/fei.jpg',
            title: '任恒飞',
            author: '猪无悔',
            date: '2020-09-25',
            press: '飞狗',
            abs: '托尼乔巴'
          },
          {
            cover: 'http://39.100.108.193/wp-content/uploads/2020/04/min.jpg',
            title: '詹为民',
            author: '猪无悔',
            date: '2020-09-25',
            press: '民狗',
            abs: '二狗'
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .cover {
    width: 115px;
    height: 172px;
    margin-bottom: 7px;
    overflow: hidden;
    cursor: pointer;
  }

  img {
    width: 115px;
    height: 172px;
    /*margin: 0 auto;*/
  }

  .title {
    font-size: 14px;
    text-align: left;
  }

  .author {
    color: #333;
    width: 102px;
    font-size: 13px;
    margin-bottom: 6px;
    text-align: left;
  }

  .abstract {
    display: block;
    line-height: 17px;
  }

  a {
    text-decoration: none;
  }

  a:link, a:visited, a:focus {
    color: #3377aa;
  }
</style>


