<template>
  <section class="bg-gray-800">
    <div
      class="px-4 py-2 flex flex-col items-center xs:flex-row xs:items-center xs:justify-between"
    >
      <div class="relative">
        <div class="absolute inset-y-0 left-0 flex items-center pl-3">
          <svg
            class="h-6 w-6 fill-current text-gray-600"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path
              d="M16.32 14.9l5.39 5.4a1 1 0 0 1-1.42 1.4l-5.38-5.38a8 8 0 1 1 1.41-1.41zM10 16a6 6 0 1 0 0-12 6 6 0 0 0 0 12z"
            />
          </svg>
        </div>
        <input
          class="pl-10 pr-4 py-2 xs:py-1 bg-gray-900 rounded-lg focus:outline-none focus:bg-gray-200 focus:text-gray-900"
          type="text"
          placeholder="Search text"
        />
      </div>
      <button
        class="block bg-gray-900 px-3 py-1 rounded-lg mt-2 xs:mt-0  flex items-center focus:outline-none focus:shadow-outline hover:bg-gray-700"
      >
        <svg
          class="h-4 w-4 fill-current text-gray-500"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
        >
          <path
            d="M17 16v4h-2v-4h-2v-3h6v3h-2zM1 9h6v3H1V9zm6-4h6v3H7V5zM3 0h2v8H3V0zm12 0h2v12h-2V0zM9 0h2v4H9V0zM3 12h2v8H3v-8zm6-4h2v12H9V8z"
          />
        </svg>
        <span class="block ml-1 text-white">Filters</span>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SearchAndFilter',
};
</script>

<style></style>
