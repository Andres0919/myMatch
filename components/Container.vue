<template>
  <div class="grid grid-cols-5 mb-32 px-10">
    <div class="col-span-2">
      <div>
        <img src="~/static/family.jpg" />
      </div>
    </div>
    <div class="col-span-3 flex flex-col justify-center text-center px-10">
      <h3 class="text-4xl mb-5">Acerca de mí</h3>
      <p>
        Vivo con mi pequeña hija y mi esposa a quienes amo, respeto y admiro por
        su manera de ser, por ayudarme a mejorar cada día en todos los aspectos.
        <br />
        Soy una persona apasionada por la tecnología, por los videojuegos y me
        gusta pasar tiempo con mi familia y amigos.
      </p>
      <!-- <span>Louie Jie Mahusay</span><br />
      <small>CEO, Founder</small> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'Container',
  components: {},
}
</script>

<style scope>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 600;
  font-size: 35px;
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
  width: 140px;
  height: 140px;
  border-radius: 50%;
}
</style>
