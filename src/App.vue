<template>
  <div id="app" class="bg-gray-200 text-gray-900 min-h-screen min-w-screen antialiased">
    <Navbar />
    <SearchAndFilter />
    <Main />
  </div>
</template>

<script>
import Navbar from "./components/Navbar/Navbar";
import SearchAndFilter from "./components/Search/SearchAndFilter";
import Main from './components/Main/Main'
export default {
  name: "App",
  components: {
    Navbar,
    SearchAndFilter,
    Main
  }
};
</script>

<style src="./assets/css/tailwind.css"/>


