<template>
  <div class="fixed w-full">
    <div class="flex justify-between bg-gray-200">
      <div class="text-gray-700 text-center bg-gray-400 px-4 py-2 my-2 ml-6">
        MyMatch
      </div>
      <div class="flex justify-between bg-gray-400 px-4 py-2 my-2">
        <div class="text-gray-700 text-center bg-gray-200 px-4 mx-2">
          1
        </div>
        <div class="text-gray-700 text-center bg-gray-200 px-4 mx-2">
          2
        </div>
        <div class="text-gray-700 text-center bg-gray-200 px-4 mx-2">
          3
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
