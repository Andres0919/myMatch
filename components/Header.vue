<template>
  <div class="fixed w-full">
    <div class="flex justify-between bg-white">
      <div class="text-gray-700 text-center bg-gray-400 px-4 py-2 my-2 ml-6">
        MyMatch
      </div>
      <div class="flex justify-between bg-white px-4 py-2 my-2">
        <div
          class="text-gray-700 text-center bg-white px-4 mx-2 hover:underline hover:text-red-800 cursor-pointer"
        >
          INICIO
        </div>
        <div
          class="text-gray-700 text-center bg-white px-4 mx-2 hover:underline hover:text-red-800 cursor-pointer"
        >
          BLOG
        </div>
        <div
          class="text-gray-700 text-center bg-white px-4 mx-2 hover:underline hover:text-red-800 cursor-pointer"
        >
          VIDEOS
        </div>
        <div
          class="text-gray-700 text-center bg-white px-4 mx-2 hover:underline hover:text-red-800 cursor-pointer"
        >
          CONTACTO
        </div>
      </div>
      <div class="text-gray-700 text-center bg-gray-400 px-4 py-2 my-2 mr-6">
        login
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Header',
  data: () => ({
    activeItem: 0,
  }),
}
</script>
