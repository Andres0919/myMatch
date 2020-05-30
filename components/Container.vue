<template>
  <div class="grid grid-cols-2 bg-gray-200 pt-12">
    <div class="col-span-2 max-h-full bg-gray-400">
      <div class="text-red-800 w-full text-center h-screen bg-gray-200">
        <div class="h-auto flex justify-center items-center img-background">
          <div class="h-full w-full overlay">
            <div class="w-full mt-24 mb-32">
              <div class="w-full flex justify-center">
                <div class="photo bg-black">
                  PHOTO
                </div>
              </div>
              <p class="font-sans font-thin text-6xl">
                ANDRÉS POSADA
              </p>
              <p class="font-mono text-2xl">
                Desarrollador web
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="text-gray-700 text-center bg-gray-400 mb-2">
        <div
          class="text-gray-700 grid grid-cols-2 text-center bg-gray-200 items-center"
        >
          <div class="px-20 mx-10">
            <ProfilePicture />
          </div>
          <p class="text-left px-10 mx-10">
            Donec molestie venenatis vulputate. Proin vitae eros vel leo pretium
            pulvinar at in neque. Integer porta vel felis eu ultricies. Nam
            mauris ex, tempor consequat ligula ut, laoreet consequat lorem.
            Donec a tristique orci. Vestibulum dapibus faucibus mi id sagittis.
            Vivamus sed turpis laoreet, dapibus metus eu, mollis ipsum.
          </p>
        </div>
        <div
          class="text-center grid grid-cols-2 bg-gray-200 px-4 mx-2 items-center"
        >
          <div>
            <p class="font-sans text-3xl text-gray-800">
              Andrés Felipe Posada Quiroz
            </p>
            <p class="font-sans text-base text-gray-500 italic">
              Tecnólogo en Sistemas de Información
            </p>
          </div>
          <div class="mt-24 px-20 mx-10">
            <SkillImg />
          </div>
        </div>
      </div>
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

.img-background {
  background-image: url('../static/background.jpg');
  background-position: center;
}

.overlay {
  background-color: rgba(0, 0, 0, 0.9);
}

.photo {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}
</style>
