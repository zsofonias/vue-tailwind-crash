<template>
  <header class="bg-gray-900">
    <div class="px-6 md:px-10 py-2 flex justify-between items-center">
      <div class="text-teal-400 font-bold text-lg">
        <span>Platform</span>
        <span class="text-gray-100">Logo</span>
      </div>
      <div>
        <div class="sm:hidden">
          <button
            v-if="isNavCollapsed"
            @click="isNavCollapsed = !isNavCollapsed"
            class="block text-gray-400 focus:outline-none focus:text-gray-200 hover:text-gray-200"
          >
            <svg
              class="h-6 w-6 fill-current"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 30 30"
            >
              <path
                d="M4 10h24a2 2 0 000-4H4a2 2 0 000 4zm24 4H4a2 2 0 000 4h24a2 2 0 000-4zm0 8H4a2 2 0 000 4h24a2 2 0 000-4z"
              />
            </svg>
          </button>
          <button
            v-if="!isNavCollapsed"
            @click="isNavCollapsed = true"
            class="block text-gray-400 focus:outline-none focus:text-gray-200 hover:text-gray-200"
          >
            <svg
              class="h-6 w-6 fill-current text-gray-400"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
            >
              <path
                d="M16.24 14.83a1 1 0 0 1-1.41 1.41L12 13.41l-2.83 2.83a1 1 0 0 1-1.41-1.41L10.59 12 7.76 9.17a1 1 0 0 1 1.41-1.41L12 10.59l2.83-2.83a1 1 0 0 1 1.41 1.41L13.41 12l2.83 2.83z"
              />
            </svg>
          </button>
        </div>

        <div class="hidden sm:flex items-center">
          <a
            href="#"
            class="block px-2 py-1 text-gray-100 hover:bg-gray-800 rounded"
          >List your Property</a>
          <a href="#" class="block ml-6 px-2 py-1 text-gray-100 hover:bg-gray-800 rounded">Trips</a>
          <a href="#" class="block ml-6 px-2 py-1 text-gray-100 hover:bg-gray-800 rounded">Messages</a>
          <AccountDropdown class="hidden sm:block ml-4 text-white" />
        </div>
      </div>
    </div>

    <!-- nav elements in mobile -->
    <div v-if="!isNavCollapsed" class="sm:hidden">
      <div class="px-3 mt-2 pb-4">
        <a
          href="#"
          class="block px-3 py-1 text-gray-100 font-medium hover:bg-gray-800 rounded-md"
        >List your Property</a>
        <a
          href="#"
          class="block px-3 py-1 my-3 text-gray-100 font-medium hover:bg-gray-800 rounded-md"
        >Trips</a>
        <a
          href="#"
          class="block px-3 py-1 text-gray-100 font-medium hover:bg-gray-800 rounded-md"
        >Messages</a>
      </div>
      <div class="mt-2 px-6 pt-4 border-t border-gray-800">
        <div class="flex items-center">
          <img
            class="block h-8 w-8 object-cover rounded-full border-2 border-teal-600"
            src="https://images.unsplash.com/photo-1537815749002-de6a533c64db?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60"
            alt="avatar image"
          />
          <p class="text-gray-200 ml-4 font-semibold">John Doe</p>
        </div>
        <div class="mt-4 pb-4">
          <a
            href="#"
            class="block py-1 px-2 text-sm text-gray-400 hover:text-gray-200"
          >Account settings</a>
          <a href="#" class="block my-2 py-1 px-2 text-sm text-gray-400 hover:text-gray-200">Support</a>
          <a href="#" class="block py-1 px-2 text-sm text-gray-400 hover:text-gray-200">Sign out</a>
        </div>
      </div>
    </div>
    <!-- nav elements in mobile end -->
  </header>
</template>

<script>
import AccountDropdown from "./AccountDropdown";
export default {
  name: "Navbar",
  components: {
    AccountDropdown
  },
  data() {
    return {
      isNavCollapsed: false
    };
  }
};
</script>

<style>
</style>