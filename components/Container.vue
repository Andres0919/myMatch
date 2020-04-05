<template>
  <div class="grid grid-cols-3 bg-gray-200 h-screen pt-12">
    <div class="col-span-2 max-h-full bg-gray-400 mr-2 overflow-y-scroll">
      <div class="text-gray-700 w-full text-center bg-gray-200 my-2">
        <h1 class="title">
          BEST CANDIDATE
        </h1>
      </div>
      <div class="text-gray-700 grid grid-cols-2 text-center bg-gray-400 mb-2">
        <div class="text-gray-700 text-center bg-gray-200 px-4 mx-2">
          <div class="mb-3">
            <ProfilePicture />
          </div>
          <p class="text-justify">
            Donec molestie venenatis vulputate. Proin vitae eros vel leo pretium
            pulvinar at in neque. Integer porta vel felis eu ultricies. Nam
            mauris ex, tempor consequat ligula ut, laoreet consequat lorem.
            Donec a tristique orci. Vestibulum dapibus faucibus mi id sagittis.
            Vivamus sed turpis laoreet, dapibus metus eu, mollis ipsum.
          </p>
        </div>
        <div class="text-center bg-gray-200 px-4 mx-2">
          <p class="font-sans text-3xl text-gray-800">
            Andrés Felipe Posada Quiroz
          </p>
          <p class="font-sans text-base text-gray-500 italic">
            Tecnólogo en Sistemas de Información
          </p>
          <div class="mt-24">
            <SkillImg />
          </div>
        </div>
      </div>
      <div
        v-for="row in 20"
        :key="row"
        class="text-gray-700 w-full text-center bg-gray-200 mb-2"
      >
        {{ row }}
      </div>
    </div>
    <div
      class="col-span-1 max-h-full text-gray-700 text-center bg-gray-400 px-4 py-2"
    >
      login
    </div>
  </div>
</template>

<script>
import ProfilePicture from '~/components/ProfilePicture'
import SkillImg from '~/components/SkillImg'

export default {
  name: 'Container',
  components: {
    ProfilePicture,
    SkillImg,
  },
}
</script>

<style scope>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 400;
  font-size: 35px;
  color: #35495e;
  letter-spacing: 1px;
  text-transform: capitalize;
}
</style>
