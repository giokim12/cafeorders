<template>
  <div>
    <b-container>
      <b-list-group-item class='list-group-item' button @click="updateSizeStatus">  
        <b-row
          class='one-size'
          :class="{ 'is-selected': size.selected }"
        >
          <b-col style="flex-grow:1;">{{ size.name }}</b-col>
          <b-col style="flex-grow:2;">{{ size.price }}원</b-col>
        </b-row>
      </b-list-group-item>  
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'SizeListItem',
  props: {
    size: Object,
  },
  methods: {
    updateSizeStatus() {
      this.$store.dispatch('updateSizeStatus', this.size)
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
</style>