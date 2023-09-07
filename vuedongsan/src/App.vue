<template>

<div class="menu">
  <a v-for="arr in 메뉴들" :key="arr">{{ arr }}</a>
</div>

<!-- 상품 목록을 어떻게 배열로 출력하지?? -->

  <div v-for="(a,i) in products" :key="i" >
    <!-- 반복되면서 0,1,2 되는 변수를 넣어주면 됨 -->
    <h4>{{a}}</h4>
    <div v-for="(a,i) in price" :key="i">
    <p>{{ price }}</p>
    </div>
    <!-- <p v-for="(a,i) in price" :key="i">{{ price }}</p> -->
  </div>
  <!-- <div>
    <h4>{{products[1]}}</h4>
    <p>{{ price2 }}</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>{{ price2 }}</p>
  </div> -->

  
</template>

<script>
// document.getElementById().innerHTML = ??;


export default {
  name: 'App',
  data(){
    return{
      //쇼핑몰의 중요한 변수 모두 저장
      메뉴들: ['Home', 'Products', 'About'],
      price: ['50 만원','가격은 아무거나','가격은 아무거나'],
      스타일: 'color : pink',
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸']
    }
  },
  components: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu{
  background:darkslateblue;
  padding:15px;
  border-radius: 5px;
}
.menu a {
  color:white;
  padding: 10px;
}
</style>
