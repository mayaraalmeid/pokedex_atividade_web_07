
<script >

import { computed, getCurrentInstance } from "@vue/runtime-core"

const axios = getCurrentInstance().appContext.config.globalProperties.axios

const props = defineProps({
    id: number,
    nome: String,
    tipo0:String,
    tipo1:String
    
})

</script>

<template>
   <div class="col">
  <div class="card shadow-sm">
      <img src =  {{this.img}} class = "card-img=top">
       <div class="card-body">
           <h5 class="card-title">{{this.nome}}</h5>
      <div class="d-flex justify-content-between align-items-center">
        <div class="btn-group">
            <button type="button" class="btn btn-sm btn-outline-secondary">{{this.tipo0}}</button>
            <button type="button" class="btn btn-sm btn-outline-secondary">{{this.tipo1}}</button>
            <a href="http://localhost:8080/pokemons/{{this.id}}" class="btn btn-danger">Mais detalhes</a>
        </div>
         </div>
     </div>
     </div>
</div>
</template>
