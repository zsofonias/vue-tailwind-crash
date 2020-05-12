<template>
  <div id="app" class="bg-gray-100 min-h-screen min-w-screen antialiased">
    <Navbar />
    <SearchAndFilter />
  </div>
</template>

<script>
import Navbar from "./components/Navbar/Navbar";
import SearchAndFilter from "./components/Search/SearchAndFilter";
export default {
  name: "App",
  components: {
    Navbar,
    SearchAndFilter
  }
};
</script>

<style src="./assets/css/tailwind.css"/>


