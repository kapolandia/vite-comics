<script setup>
  import AppHeader from './components/AppHeader.vue'
  import HomeJumbotron from './components/HomeJumbotron.vue'
  import ComicsGrid from './components/ComicsGrid.vue';
  import AppIcons from './components/AppIcons.vue';
  import AppNav from "./components/AppNav.vue"
	import AppContacts from "./components/AppContacts.vue"
</script>

<template>
  <AppHeader></AppHeader>
  <HomeJumbotron></HomeJumbotron>
  <ComicsGrid></ComicsGrid>
  <AppIcons></AppIcons>
	<footer>
		<AppNav></AppNav>
		<AppContacts></AppContacts>
	</footer>
</template>

<style lang="scss">
	@use "./style/generic";
</style>
