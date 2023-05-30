<template>
  <form id="movies" action="http://localhost:3000/api" method="post">
    <label for="date">Date</label>
    <input type="date" id="date" name="date">
    <label for="name">Name</label>
    <input type="text" id="name" name="name">
    <label for="price">Price</label>
    <input type="text" id="price" name="price">
    <button type="submit">Submit</button>
    <button type="button" onclick="window.location.href=('show.html')">Show</button>
  </form>


  <table id="table"></table>

</template>

<script>
export default {
  data() {
    return {
      date: '',
      name: '',
      price: '',
    }
  },

  method: {
    addItem() {
      let item = {
        Date: this.date,
        product: this.name,
        Price: this.price
      }
      this.table.push(item);
      this.date = '';
      this.name = '';
      this.price = '';
    }
  }
}
</script>

<style scoped>

</style>