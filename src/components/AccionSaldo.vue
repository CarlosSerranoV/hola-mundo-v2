<template>
<button v-on:click="aumentar" :disabled="mostrar">{{ texto }}</button>
</template>

<script>
export default {
  data(){

  },
  props:{
    texto: String,
    mostrar: {
      type: Boolean,
      default:false
    }

  },
  methods:{
    aumentar(){
      this.$emit('accion');
    }
  }
}
</script>