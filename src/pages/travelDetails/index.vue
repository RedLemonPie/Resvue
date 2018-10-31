<template>
  <div>
      <detailSlider></detailSlider>
      <detailHeader></detailHeader>
      <orderChoice></orderChoice>
  </div>
</template>

<script>
import detailSlider from './detailSlider'
import detailHeader from './header'
import orderChoice from './orderChoice'

export default {
  components: {
    detailSlider,
    detailHeader,
    orderChoice
  },
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<style>

</style>
