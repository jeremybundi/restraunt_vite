<template>
  <div class="bg-gradient-to-r from-indigo-900 to-blue-600 text-white py-4">
    <!-- Top Section with Logo, Title, Centered Links, and Login Button -->
    <div class="container mx-auto flex flex-col md:flex-row items-center justify-between px-4">
      <div class="flex items-center mb-2 md:mb-0 md:w-auto"> <!-- Logo on the left -->
        <img src="../assets/1.jpg" alt="Logo" class="h-14 mr-2 rounded-full" /> <!-- Logo with curved edges -->
      </div>
      <div class="flex-1 mb-2 md:mb-0 flex justify-center"> <!-- Centering the title -->
        <span class="text-3xl font-bold font-sans">Ufanisi Resort</span> <!-- Title -->
      </div>
      <div class="flex-1 mb-2 md:mb-0 flex justify-center"> <!-- Centering the navigation links -->
        <div class="flex space-x-8">
          <a href="#" class="text-sm hover:underline">Destinations</a>
          <a href="#" class="text-sm hover:underline">Offers</a>
          <a href="#" class="text-sm hover:underline">Meetings & Events</a>
          <a href="#" class="text-sm hover:underline">Brands</a>
        </div>
      </div>
      <div class="flex-shrink-0 mb-2 md:mb-0"> <!-- Ensure buttons do not shrink -->
        <button class="bg-white text-indigo-600 py-1 px-4 rounded-full hover:bg-indigo-100">
          Login
        </button>
      </div>
    </div>

    <!-- Bottom Section for Additional Links (Optional) -->
    <div class="bg-indigo-800 py-3 mt-4 rounded-lg">
      <div class="container mx-auto text-center">
        <div class="flex flex-col md:flex-row justify-center items-center space-y-2 md:space-y-0 md:space-x-8">
          <!-- Optional additional links can go here -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopBarComponent",
};
</script>

<style scoped>
/* Custom gradient background and button hover effect */
.bg-gradient-to-r {
  background: linear-gradient(to right, #1e3a8a, #3b82f6); /* Dark indigo to blue */
}

button {
  transition: background-color 0.3s ease;
}

/* Add font-family for title if needed */
.font-sans {
  font-family: 'Scans', sans-serif; /* Replace 'Scans' with the actual font you want to use */
}
</style>
