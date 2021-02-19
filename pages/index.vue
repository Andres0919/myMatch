<template>
  <div>
    <Header />
    <Container />
    <div class="flex justify-center">
      <hr class="divider text-primary" />
    </div>
    <div class="grid grid-cols-5 px-20 mt-20">
      <div class="col-span-3 flex justify-center flex-col pl-10">
        <h3 class="text-4xl mb-5">¿Actualmente qué hago?</h3>
        <ul class="list-disc">
          <li>Actualmente estoy trabajando con Nestjs y Vue3 js</li>
          <li>Actualmente estoy aprendiendo TypeScript y Golang</li>
          <li>
            Actualmente estoy leyendo
            <em>`Seven databases in seven weeks`</em>
          </li>
          <li>Actualmente estoy viendo <em>`Barbarians`</em></li>
          <li>Pregunteme sobre Javascript - Vue(Nuxt), Express</li>
        </ul>
      </div>
      <div class="col-span-2 flex items-center">
        <div>
          <img src="~/static/dev.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Container from '~/components/Container.vue'
import Header from '~/components/Header.vue'

export default {
  components: {
    Container,
    Header,
  },
}
</script>

<style>
.divider {
  width: 20%;
  border: 1px solid;
}
</style>
