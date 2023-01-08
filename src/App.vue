<template>
  <div id="app" class="main-container">
    <PageContent msg="Dashboard"/>
    <SideBar />
  </div>
</template>

<script>
import PageContent from './components/PageContent.vue'
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: { PageContent, SideBar }
}
</script>

<style lang="scss">
@import '@/assets/css/variables.scss';
.main-container {
    display: flex;
    flex-direction: row-reverse;
    width: 100%;
    height: 100%;
    color: $base-purple;
}
</style>
