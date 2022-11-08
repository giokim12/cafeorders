<template>
  <div>
    <b-container>
      <b-list-group-item class='list-group-item' button @click="updateMenuStatus">  
        <b-row 
          class='one-menu'
          :class="{ 'is-selected': menu.selected }"
        >
        
          <b-col style="flex-grow:1;"><img style= "width: 50px; height: 50px" :src="menu.image"></b-col>
          <b-col>{{ menu.title }}</b-col>
          <b-col style="flex-grow:2;">{{ menu.price }}원</b-col>
        </b-row>
      </b-list-group-item>  
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'MenuListItem',
  data() {
    return {
      menu: null
    }
  },
  props: {
    menu: Object,
  },
  methods: {
    updateMenuStatus() {
      this.$store.dispatch('updateMenuStatus', this.menu)
    }
  }

}
</script>

<style>
  .is-selected {
    background-color: green;
    color: white;
    padding: none;
    /* border: none; */
  }
  /* .one-menu {
    display: flex;
    flex-direction: row;
    flex-grow: 1;
  } */

</style>