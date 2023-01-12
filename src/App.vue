<script>
import AppContent from './components/AppContent.vue';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,

  }
}
</script>

<template>

  <AppHeader />
  <AppContent />
  <AppFooter />


</template>


<style lang="scss">
@use './styles/generals.scss' as *;
</style>