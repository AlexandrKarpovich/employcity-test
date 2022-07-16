<template>
  <div class="order">
    <MainBanner />
    <OrderForm />
  </div>
</template>


<script>
import MainBanner from '../components/MainBanner.vue'
import OrderForm from '../components/OrderForm.vue'
export default {
  name: 'OrderView',
  components: {
    MainBanner,
    OrderForm
}
}
</script>

