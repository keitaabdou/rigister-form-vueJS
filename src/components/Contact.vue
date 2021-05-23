<template>
  <div class="hello">
  <h1>Formulaire D'Inscription</h1>
    <div class="mt-5">
          <p v-if="output[0]">Nom:{{output[0]}}</p>
          <p v-if="output[1]">Prénom:{{output[1]}}</p>
          <p v-if="output[2]">Email:{{output[2]}}</p>
          <p v-if="output[3]">Numéro:{{output[3]}}</p>
    </div>
    <div class="bg-white  max-w-lg mx-auto md:p-12 my-10 rounded-lg shadow-2xl">
            <form class="flex flex-col mt-2" method="POST" action="#">
                <div class="mb-6 pt-3 rounded bg-gray-200 text-2xl">
                    <input type="text" v-model="nom" placeholder="Entrer votre nom" class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-gray-300 px-3 pb-3">
                </div>
                <div class="mb-6 pt-3 rounded bg-gray-200 text-2xl">
                    <input type="text" v-model="prenom" placeholder="Entrer votre prenom" class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-gray-300 px-3 pb-3">
                </div>
                <div class="mb-6 pt-3 rounded bg-gray-200 text-2xl">
                    <input type="email" v-model="email" placeholder="Votre email" class="bg-gray-200 rounded w-full text-gray-700 focus:outline-none border-gray-300 px-3 pb-3">
                </div>
                <div class="mb-6 pt-3 rounded bg-gray-200 text-2xl">
                    <input type="tel" v-model="numero" placeholder="Entrez votre numero" class="bg-gray-200  rounded w-full text-gray-700 focus:outline-none  border-gray-300 px-3 pb-3">
                </div>
                <button class="bg-blue-600 hover:bg-purple-700 text-white font-bold py-2 rounded shadow-lg hover:shadow-xl transition duration-200" @click.prevent="inscription" type="submit">Valider</button>
            </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data(){
    return{
      nom:"",
      prenom:"",
      email: "",
      numero: "",
      output:""
    }
  },
  methods: {
    inscription(){

      this.output = [
        this.nom,
        this.prenom,
        this.email,
        this.numero
        
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
