<template>
  <div class="relative">
    <button @click="isOpen = !isOpen" class="relative z-10 block focus:outline-none">
      <img
        class="block h-8 w-8 object-cover rounded-full border-2 border-teal-600"
        src="https://images.unsplash.com/photo-1537815749002-de6a533c64db?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60"
        alt="avatar image"
      />
    </button>
    <button
      v-if="isOpen"
      @click="isOpen = false"
      tabindex="-1"
      class="fixed inset-0 h-full w-full cursor-default focus:outline-none"
    ></button>
    <div
      v-if="isOpen"
      class="absolute right-0 mt-2 w-40 py-2 bg-white text-sm text-gray-900 rounded shadow overflow-hidden"
    >
      <a href="#" class="block px-4 py-2 hover:bg-teal-600 hover:text-gray-100">Account settings</a>
      <a href="#" class="block px-4 py-2 hover:bg-teal-600 hover:text-gray-100">Support</a>
      <a href="#" class="block px-4 py-2 hover:bg-teal-600 hover:text-gray-100">Sign out</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "AccountDropdown",
  data() {
    return {
      isOpen: false
    };
  },

  created() {
    const handleEscKey = e => {
      if (e.key === "Esc" || e.key === "Escape") {
        this.isOpen = false;
      }
    };
    document.addEventListener("keydown", handleEscKey);
    this.$once("hook:beforeDestroy", () => {
      document.removeEventListener("keydown", handleEscKey);
    });
  }
};
</script>

<style>
</style>