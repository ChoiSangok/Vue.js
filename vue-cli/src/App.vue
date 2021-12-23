<template>
  <div>
      <!-- <app-header v-bind:프롭스 속성이름="상위 컴포넌트의 데이터 이름"></app-header> -->
      <app-header v-bind:propsdata="str"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

var AppHeader = {
    template: '<header>Header</header>'
}
export default {
    data: function() {
        return {
            str: 'header'
        }
    },
    components: {
        'app-header': AppHeader
    }
}
</script>

<style>

</style>