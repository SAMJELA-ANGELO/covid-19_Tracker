<template>
  <HeaderTab/>
  <div class="container mx-auto">
    
    <router-view/>
  </div>
</template>

<script>
import HeaderTab from './components/HeaderTab.vue';


export default{
  components:{
    HeaderTab,
},
}
</script>