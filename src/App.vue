<template>
  <div id="app">
    <headBar />
    <div class = "main">
      <div class = "sidebar">
        <NotificationButton />
        <SidebarMenu />
      </div>
      <Dashboard/>
    </div>
  </div>
</template>

<script>
import Dashboard from './components/Dashboard.vue';
import SidebarMenu from './components/SidebarMenu.vue';
import HeadBar from './components/HeadBar.vue';
import NotificationButton from './components/NotificationButton.vue'

export default {
  name: 'App',
  components:{
    Dashboard,
    SidebarMenu,
    HeadBar,
    NotificationButton,
  },
};
</script>

<style>
.app{
  background: #F0F2F5;
}

html, 
body {
    margin: 0;
    padding: 0;
    background: #F0F2F5;
}

.main{
  display: flex;
  justify-content: space-evenly;
}

.sidebar{
  flex-direction: column;
  display: flex;
}


</style>