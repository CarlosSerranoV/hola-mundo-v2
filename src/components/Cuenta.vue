<template>
  <h2>Tipo de cuenta: {{ cuenta }}</h2>
  <h2>Saldo: {{ saldo }} </h2>
  <h2>Cuenta: {{ estado ? 'Activa' : 'Desactivada' }}</h2>
  <div v-for="(servicio, index) in servicios" :key="index">
    {{ index + 1 }} - {{ servicio }}
  </div>
  <accion-saldo texto="Aumentar saldo" @accion="aumentar"></accion-saldo>
  <accion-saldo texto="Disminuir saldo" @accion="disminuir" :mostrar="mostrar"></accion-saldo>

</template>

<script>
import accionSaldo from './AccionSaldo'

export default {
  data() {
    return {
      saldo: 1000,
      cuenta: 'Visa',
      estado: true,
      servicios: ['giro', 'abono', 'transferencia'],
      mostrar: false
    }
  },
  components:{
    accionSaldo

  },
  methods:{
    aumentar(){
      this.saldo += 100;
      this.mostrar = false;

    },
    disminuir(){
      if(this.saldo === 0){
        this.mostrar = true;

        alert('No se puede disminuir mas');
      }else{
      this.saldo -= 100
      }

    }
  }
}
</script>