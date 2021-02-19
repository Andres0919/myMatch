<template>
  <header class="h-screen">
    <nav class="grid grid-cols-3 mt-6">
      <div class="col-span-1 flex justify-center">
        <div class="text-4xl font-bold">
          <a href="/"><span class="text-black">AP</span>. </a>
        </div>
      </div>
      <div class="col-span-2 flex items-center justify-around">
        <ul class="flex">
          <li class="mx-5"><a href="">Home</a></li>
          <li class="mx-5">Acerca de mi</li>
          <li class="mx-5">Portafolio</li>
          <li class="mx-5">Blog</li>
          <li class="mx-5">Contacto</li>
          <li class="mx-3 px-3 bg-primary rounded-full">
            <a href="#" class="hover:shadow-2xl">
              <span class="text-white">
                Login
              </span>
            </a>
          </li>
        </ul>
      </div>
    </nav>
    <div class="h-full flex justify-center flex-col items-center">
      <h1 class="text-5xl">Hola, soy Andrés Posada</h1>
      <h2 class="text-3xl">
        Desarrollador web
        <span class="text-secondary">JavaScript</span>
        de Colombia
      </h2>
      <p class="mt-16">
        <a class="btn-lg btn-primary" href="#">GitHub</a>
        <a class="btn-lg btn-secondary">LinkedIn</a>
      </p>
    </div>
  </header>
</template>
<script>
export default {
  name: 'Header',
  data: () => ({
    activeItem: 0,
  }),
}
</script>
<style scoped></style>
