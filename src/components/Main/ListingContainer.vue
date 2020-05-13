<template>
  <div class="px-4 py-6">
    <div>
      <h3 class="font-semibold text-lg">Los Angeles</h3>
      <p class="mt-1 xs:text-sm text-gray-600 leading-4">
        Live like the stars in these luxurious Southern Califonia estates.
      </p>
    </div>
    <div class="mt-6 px-2 flex justify-center ">
      <Listing />
    </div>
  </div>
</template>

<script>
import Listing from './Listing';
export default {
  name: 'ListingContainer',
  components: {
    Listing,
  },
};
</script>

<style></style>
