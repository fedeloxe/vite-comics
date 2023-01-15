<script>
import AppContent from './components/AppContent.vue';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from './components/AppJumbo.vue';


export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
    AppJumbo,

  }
}
</script>

<template>

  <AppHeader />
  <AppJumbo />
  <AppContent />
  <AppFooter />


</template>


<style lang="scss">
@use './styles/generals.scss' as *;
</style>