<template>
  <div>
    <!--巢狀menu  直+橫-->
    <nav class="main-nav">
      <ul>
        <li class="menu-item">
          <a href="" >國家</a> <!-- 第一層 hover -->
          <ul class="sub-menu"> <!-- 子項目 show 直式 menu -->
            <li class="sub-menu-item">
              <a href="">亞洲</a>
              <ul>
                <li>
                  <a href="">韓國</a>
                </li>
                <li>
                  <a href="">日本</a>
                </li>
                <li>
                  <a href="">泰國</a>
                </li>
                <li>
                  <a href="">台灣</a>
                </li>
                <li>
                  <a href="">香港</a>
                </li>
              </ul>
            </li>
            <li class="sub-menu-item">
              <a href="">歐洲</a>
              <ul>
                <li>
                  <a href="">英國</a>
                </li>
                <li>
                  <a href="">法國</a>
                </li>
                <li>
                  <a href="">義大利</a>
                </li>
                <li>
                  <a href="">羅馬</a>
                </li>
                <li>
                  <a href="">瑞士</a>
                </li>
              </ul>
            </li>
            <li class="sub-menu-item">
              <a href="">非洲</a>
              <ul>
                <li>
                  <a href="">北非</a>
                </li>
                <li>
                  <a href="">剛果</a>
                </li>
                <li>
                  <a href="">黃金海岸</a>
                </li>
                <li>
                  <a href="">南非</a>
                </li>
                <li>
                  <a href="">波札那</a>
                </li>
              </ul>
            </li>
          </ul>
        </li>
         <li class="menu-item">
          <a href="">國家2</a> <!-- 第一層 hover -->
        </li>
         <li class="menu-item">
          <a href="">國家3</a> <!-- 第一層 hover -->
        </li>
      </ul>
    </nav>
  </div>
</template>
<script>
import _ from 'lodash'
export default {
  setup () {
    const lodashArray = [1, 2, 3, 4, 5, 6]

    const lodashResult = _.chain(lodashArray).filter(i => i > 3).value()
    console.log(lodashResult) // [4 ,5 ,6]
    return {
    }
  }
}
</script>
<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
  list-style: none;
}
.main-nav{
  background: #fa0;
}
.main-nav a{
  color: #fff;
  display: block;
  padding: 10px 20px;
  text-decoration: none;
}
.sub-menu-item > a{
  color: red;
}
.main-nav > ul{
  display: flex;
  justify-content: center;
}
.menu-item:hover .sub-menu{ //用hover 控制
  display: flex;
}
.sub-menu{
  display: none;
  position: absolute;
  background: #faf;
  // display: flex;
}

</style>
