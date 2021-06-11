<template>
  <div>
    <Header />
    <Container />
    <div class="flex justify-center">
      <hr class="divider text-primary" />
    </div>
    <div class="grid grid-cols-5 my-20">
      <div class="col-span-5">
        <h3 class="text-4xl text-center mb-6">
          ¿Qué dicen otras personas de mí?
        </h3>

        <div class="flex justify-around h-56">
          <template v-for="(item, i) in itemsCarousel">
            <div
              v-if="item && item.id"
              :key="i"
              class="flex flex-col border rounded-lg bg-primary text-white p-5 m-2 w-1/4 h-full"
            >
              <div class="w-10 h-10 rounded-full bg-primary text-white mb-4">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M18 13V5a2 2 0 00-2-2H4a2 2 0 00-2 2v8a2 2 0 002 2h3l3 3 3-3h3a2 2 0 002-2zM5 7a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1zm1 3a1 1 0 100 2h3a1 1 0 100-2H6z"
                    clip-rule="evenodd"
                  />
                </svg>
              </div>
              <div class="flex flex-col justify-between h-full">
                <p class="text-base">{{ item.comment }}</p>
                <div class="mt-2 relative bottom-0 w-full">
                  <span
                    class="flex justify-end items-center leading-none text-sm mr-6"
                  >
                    {{ item.fullName }}
                  </span>
                </div>
              </div>
            </div>
          </template>
        </div>
        <p class="text-sm text-center m-6">
          ¿Me conoces?
          <button class="text-primary" @click="showModal = true">
            Escribe algo sobre mí
          </button>
        </p>
      </div>
    </div>
    <div class="flex justify-center">
      <hr class="divider text-primary" />
    </div>
    <div class="grid grid-cols-5 px-20 my-20">
      <div class="col-span-3 flex justify-center flex-col pl-10">
        <h3 class="text-4xl mb-5">¿Actualmente qué hago?</h3>
        <ul class="list-disc">
          <li>Estoy trabajando con Nestjs y Vuejs</li>
          <li>Estoy aprendiendo TypeScript y Golang</li>
          <li>
            Estoy leyendo
            <em>`Seven databases in seven weeks`</em>
          </li>
          <li>Estoy viendo <em>`Barbarians`</em></li>
          <li>Pregunteme sobre Javascript - Vue(Nuxt), Express</li>
        </ul>
      </div>
      <div class="col-span-2 flex items-center">
        <div>
          <img src="~/static/dev.svg" />
        </div>
      </div>
      <div class="col-span-3 mt-6">
        <p class="flex justify-around" align="left">
          <img
            src="https://www.vectorlogo.zone/logos/w3_html5/w3_html5-icon.svg"
            alt="html5"
            title="HTML5"
            width="40"
            height="40"
          />
          <img
            src="https://cdn.icon-icons.com/icons2/2415/PNG/512/css_original_logo_icon_146575.png"
            alt="css3"
            title="CSS3"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/javascript/javascript-icon.svg"
            alt="javascript"
            title="Javascript"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/vuejs/vuejs-icon.svg"
            alt="vuejs"
            title="Vuejs"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/nuxtjs/nuxtjs-icon.svg"
            alt="nuxtjs"
            title="Nuxtjs"
            width="40"
            height="40"
          />
          <img
            src="https://www.chartjs.org/media/logo-title.svg"
            alt="chartjs"
            title="Chartjs"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/linux/linux-icon.svg"
            alt="linux"
            title="Linux"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/nodejs/nodejs-icon.svg"
            alt="nodejs"
            title="Nodejs"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/expressjs/expressjs-ar21.svg"
            alt="express"
            title="Expressjs"
            width="40"
            height="40"
          />
          <img
            src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg"
            alt="git"
            title="Git"
            width="40"
            height="40"
          />

          <img
            src="https://www.vectorlogo.zone/logos/mysql/mysql-icon.svg"
            alt="mysql"
            title="MySQL"
            width="40"
            height="40"
          />

          <img
            src="https://www.vectorlogo.zone/logos/postgresql/postgresql-icon.svg"
            alt="postgresql"
            title="PostgreSQL"
            width="40"
            height="40"
          />
        </p>
      </div>
    </div>
    <transition
      enter-active-class="transition duration-300"
      enter-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition duration-300"
      leave-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <div
        v-show="showModal"
        class="fixed inset-0 w-full h-full z-20 bg-black bg-opacity-50 duration-300 overflow-y-auto"
      >
        <div
          class="relative sm:w-3/4 md:w-3/5 lg:w-3/5 mx-2 sm:mx-auto my-10 opacity-100"
        >
          <transition
            enter-active-class="transition transform duration-300"
            enter-class="scale-0"
            enter-to-class="scale-100"
            leave-active-class="transition transform duration-300"
            leave-class="scale-100"
            leave-to-class="scale-0"
          >
            <div
              v-show="showModal"
              class="relative bg-white shadow-lg rounded-md text-gray-900 z-20"
            >
              <header class="flex items-center justify-between py-2 px-5">
                <h2 class="font-semibold">Escribe sobre mí</h2>
                <button
                  class="focus:outline-none p-2"
                  @click="showModal = false"
                >
                  <svg
                    class="fill-current"
                    xmlns="http://www.w3.org/2000/svg"
                    width="18"
                    height="18"
                    viewBox="0 0 18 18"
                  >
                    <path
                      d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"
                    ></path>
                  </svg>
                </button>
              </header>
              <main class="py-2 px-5">
                <p class="text-sm font-semibold px-3">
                  Lo que escribas sobre mí todo el que visite mi sitio web lo
                  podrá ver :)
                </p>
                <div class="grid">
                  <div class="col-span-1 px-3 mb-5">
                    <label for="" class="text-xs font-semibold px-1">
                      ¿Cúal es tu nombre?
                    </label>
                    <div class="flex justify-center">
                      <div
                        class="w-10 z-10 pl-1 text-center pointer-events-none flex items-center justify-center"
                      >
                        <i
                          class="mdi mdi-account-outline text-gray-400 text-lg"
                        ></i>
                      </div>
                      <input
                        v-model="form.fullName"
                        type="text"
                        class="w-full -ml-10 pl-10 pr-3 py-2 rounded-lg border-2 border-gray-200 outline-none focus:border-primary"
                        placeholder=""
                      />
                    </div>
                  </div>
                  <div class="col-span-1 px-3 mb-5">
                    <label for="" class="text-xs font-semibold px-1">
                      Comentario sobre mí
                    </label>
                    <div class="flex">
                      <div
                        class="w-10 z-10 pl-1 text-center pointer-events-none flex items-center justify-center"
                      >
                        <i
                          class="mdi mdi-account-outline text-gray-400 text-lg"
                        ></i>
                      </div>
                      <textarea
                        v-model="form.comment"
                        type=""
                        class="w-full -ml-10 pl-10 pr-3 py-2 rounded-lg border-2 border-gray-200 outline-none focus:border-primary"
                        placeholder=""
                      >
                      </textarea>
                    </div>
                  </div>
                  <label class="flex justify-start items-start px-3">
                    <div
                      class="bg-white border-2 rounded border-gray-400 w-6 h-6 flex flex-shrink-0 justify-center items-center mr-2 focus-within:border-blue-500"
                    >
                      <input
                        v-model="form.authorizeSocial"
                        type="checkbox"
                        class="opacity-0 absolute"
                      />
                      <svg
                        class="fill-current hidden w-4 h-4 text-green-500 pointer-events-none"
                        viewBox="0 0 20 20"
                      >
                        <path d="M0 11l2-2 5 5L18 3l2 2L7 18z" />
                      </svg>
                    </div>
                    <div class="select-none text-sm font-semibold">
                      ¿Autoriza publicar las redes sociales donde te sigo, como
                      Twitter o Linkedin?
                    </div>
                  </label>
                </div>
              </main>
              <footer class="flex justify-around p-2">
                <button class="hover:bg-gray-300 p-2 w-32 rounded">
                  Cancelar
                </button>
                <button
                  class="bg-primary opacity-75 font-semibold text-white p-2 w-32 rounded hover:bg-primary hover:opacity-100 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300"
                  @click="sendOpinion()"
                >
                  Enviar
                </button>
              </footer>
            </div>
          </transition>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
import Container from '~/components/Container.vue'
import Header from '~/components/Header.vue'

const initForm = () => ({
  fullName: '',
  comment: '',
  authorizeSocial: false,
})

export default {
  components: {
    Container,
    Header,
  },
  data: () => {
    return {
      showModal: false,
      itemsActive: 5,
      comments: [],
      form: initForm(),
    }
  },
  computed: {
    itemsCarousel() {
      if (this.comments.length === 0) {
        return
      }

      let pos = this.itemsActive
      const totalShow = 3
      let items = []
      for (let i = 0; i < totalShow; i++) {
        if (pos >= this.comments.length) {
          pos = 0
        }
        const itemFound = items.find(
          (item) => item.id === this.comments[pos].id
        )
        items = !itemFound ? [...items, this.comments[pos]] : items
        pos++
      }
      return items
    },
  },
  created() {
    this.fetchOpinions()
  },
  methods: {
    async fetchOpinions() {
      try {
        const { data } = await this.$axios.get('/opinions')
        this.comments = data.body
      } catch (error) {
        console.error(error.message)
      }
    },
    async sendOpinion() {
      try {
        const { data } = await this.$axios.post('/opinions', this.form)
        this.showModal = false
        this.form = initForm()
      } catch (error) {
        console.error(error.message)
      }
    },
  },
}
</script>

<style>
.divider {
  width: 20%;
  border: 1px solid;
}

input:checked + svg {
  display: block;
}
</style>
