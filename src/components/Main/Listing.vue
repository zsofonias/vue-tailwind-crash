<template>
  <div class="w-72 xxs:w-84 max-w-84">
    <div class="relative pb-3/4">
      <img
        class="absolute h-full w-full object-cover rounded-lg"
        src="../../assets/img/pic-1.jpg"
        alt="image alt"
      />
    </div>
    <div class="relative px-3 -mt-16">
      <div class="bg-white px-4 py-3 rounded-lg shadow-md">
        <div class="flex items-center">
          <span class="bg-teal-300 text-teal-800 rounded-full px-2  text-sm"
            >New</span
          >
          <span
            class="ml-2 text-gray-600 text-xs font-bold uppercase tracking-wide"
            >3 beds &bull; 2 baths</span
          >
        </div>
        <h3 class="mt-2 font-semibold leading-4 truncate">
          Modern home in city center fjlskadf sfasdjfsdlfjlasdf asdflasdjf
        </h3>
        <p class="mt-1">
          $1,400 <span class="text-gray-600 text-sm">/wk</span>
        </p>
        <div class="mt-2 flex items-center">
          <svg
            v-for="i in 5"
            :key="i"
            :class="i <= rating ? 'text-teal-500' : 'text-gray-500'"
            class="h-4 w-4 fill-current"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
          >
            <path
              d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"
            />
          </svg>
          <p class="ml-2 text-sm text-gray-600">34 Reviews</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Listing',
  data() {
    return {
      rating: 4,
    };
  },
};
</script>

<style></style>
