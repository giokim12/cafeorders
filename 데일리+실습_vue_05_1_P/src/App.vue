<template>
  <div id="app">
    <b-container class="bv-example-row coffee-order">
      <h1>Coffee Order App</h1>
      <b-row class="outerbox">
        <b-col class="innerbox">
          <MenuList/>
          <MenuListItem/>
        </b-col>
        <!-- <b-col><SizeList/></b-col> -->
        <b-col class="innerbox">
          <SizeList/>
          <SizeListItem/>
        </b-col>
      </b-row>
    </b-container>
    
    <b-container class="bv-example-row coffee-order">
        <OrderList/>
    </b-container>

  <div>
    
  </div>
    
  </div>
</template>

<script>
import MenuList from '@/components/MenuList'
import MenuListItem from '@/components/MenuListItem'
import SizeList from '@/components/SizeList'
import SizeListItem from '@/components/SizeListItem'
import OrderList from '@/components/OrderList'


export default {
    name: 'App',
    components: {
        MenuList,
        MenuListItem,
        SizeList,
        SizeListItem,
        OrderList,
    },
    methods: {
      


    }
}
</script>



<style>
* {
  box-sizing: border-box;
  font-family: 'Noto Sans KR', sans-serif;
  padding: 0;
  margin: 0;
}

ul {
  list-style: none;
}


</style>
