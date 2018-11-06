<template>
<div class="row">
  <div id="home" class="col-sm-12 text-center">
    <div class="background">
      <h1>Welcome to Tutto Bello</h1>
      <h2>Pizza Order</h2>
      
      <div class="col-sm-12 col-md-8">
		<table class="table" border="1" style="margin: auto;width: 40%;background-color: #ffffff;">
			<thead class="thead-default">
				<tr>
					<th align="left"><strong>Pizza</strong></th>
					<th align="left"><strong>Price</strong></th>
					<th align="center"><strong>Quantity</strong></th>
				</tr>
			</thead>
			<tbody v-for="pizza in menuItems" :key="pizza.name">
				<tr>
					<td ><b><strong>{{pizza.name}}</strong></b></td>
				</tr>
				<tr v-for="opt in pizza.opts" :key="opt.size">
					<td>{{opt.size}}</td>
					<td>{{opt.price}}</td>
					<td align="center"><quantity-button></quantity-button></td>
				</tr>
			</tbody>
		</table>
  </div>
    </div>

  </div>
</div>
</template>

<script>
export default {
    name: 'PizzaBooking',
    data () {
        return {
            menuItems: [{name: 'DIAVOLA', opts: [{size: 'Large', price: '149 kr'}, {size: 'Regular', price: '119 kr'}]},
            {name: 'MARGHERITA', opts: [{size: 'Large', price: '140 kr'}, {size: 'Regular', price: '99 kr'}]},
            {name: 'NAPOLETANA', opts: [{size: 'Large', price: '149 kr'}, {size: 'Regular', price: '115 kr'}]}]
        }
    }
}
</script>

<style>
#home{
  background: url('https://i2.wp.com/www.splendidcomms.com/wp-content/uploads/2018/07/Dominos.jpg');
  height: 88vh;
  padding: 30px;
}
h1,h2{
  margin: 4% auto;
  text-align: center;
}
.background{
  background: rgba(255,255,255,.1);
  padding: 40px 0;
}
</style>