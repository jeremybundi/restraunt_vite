<template>
  <div>
    <TopBar />

    <!-- Main Section with Image and Map -->
    <div class="flex flex-col md:flex-row items-start justify-between bg-gray-100 py-8 px-4">
      <!-- Map Column -->
      <div class="w-full md:w-1/4 h-full p-4 bg-white shadow-lg rounded-lg mb-4 md:mb-0">
        <h3 class="text-xl font-bold mb-4 text-center">Our Location</h3>
        <!-- Google Map Embed -->
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3151.8354345093716!2d144.95592731584414!3d-37.817209442021675!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ad642af0f11fd81%3A0xf5779df99b6d8194!2sResort!5e0!3m2!1sen!2s!4v1648905841404!5m2!1sen!2s" 
          width="100%" 
          height="300" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy">
        </iframe>

        <!-- Location Information -->
        <div class="mt-4">
          <p class="text-gray-700 text-sm">
            <strong>Address:</strong> 123 Resort Lane, Paradise City, 45678
          </p>
          <p class="text-gray-700 text-sm">
            <strong>Phone:</strong> +123 456 7890
          </p>
          <p class="text-gray-700 text-sm">
            <strong>Email:</strong> info@resort.com
          </p>
        </div>
      </div>

      <!-- Image Column -->
      <div class="relative w-full md:w-3/4 h-auto overflow-hidden rounded-lg shadow-lg">
        <!-- Sliding Text Overlay -->
        <div class="absolute inset-0 flex items-center justify-center">
          <div class="w-full">
            <p class="text-4xl md:text-5xl font-bold font-serif text-white text-center animate-slide">
              Welcome To Ufanisi Resort
            </p>
          </div>
        </div>

        <!-- Main Image -->
        <img
          src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/454703093.jpg?k=1dcf50ae6c58dc4e093a6ddf7bd712086fbeb7ac9f2506dca6a860b0679d68f2&o=&hp=1"
          alt="Hotel Image"
          class="w-full h-96 object-cover"
        />

        <!-- Small Images Below Main Image -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-2 mt-4">
          <img src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/454703139.jpg?k=7f6d4e40616aeb758df200b01f74286c0e800a87df8f270b5ff4eb27a7fdf4f7&o=&hp=1" class="w-full h-32 object-cover rounded-lg" />
          <img src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/454702929.jpg?k=62a4ae1b060c20f75c645cca8b610c028580a13bb8480b86a4c957933db4b8d3&o=&hp=1" class="w-full h-32 object-cover rounded-lg" />
          <img src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/454703169.jpg?k=02bd56a218bd9f0481477a3255cab0dc62906708e1de592a3032bc34bc8943ca&o=&hp=1" class="w-full h-32 object-cover rounded-lg" />
          <!-- View More with Text Overlay -->
          <div class="relative w-full h-32">
            <img src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/454711896.jpg?k=601e18a29f201a7cfb9904dc09fc3ab38aad4c4ad2a5ad1c7caf506ed87d4369&o=&hp=1" class="w-full h-full object-cover rounded-lg" />
            <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center rounded-lg">
              <span class="text-white text-xl font-bold">View More</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from './Footer.vue';
import TopBar from './TopBar.vue';

export default {
  name: "ImageComponent",
  components: {
    FooterComponent, 
    TopBar,
  },
};
</script>

<style scoped>
/* Custom styles for the component */
h3 {
  color: #2c3e50;
}

/* Sliding Text Animation */
@keyframes slide {
  0% {
    transform: translateX(100%);
  }
  50% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%);
  }
}

.animate-slide {
  animation: slide 15s linear infinite alternate;
}
</style>
