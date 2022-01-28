<template>
  <div>
    <h1> Quantidade de pessoas: {{quantidade}} </h1>
   <v-btn
      class="mx-2"
      fab
      dark
      color="green"
      @click="quantidade += 1">

      <v-icon >
        mdi-plus
      </v-icon>

    </v-btn>
  
     <v-btn
    
      class="mx-2"
      fab
      dark
      color="red"
      @click="quantidade -= 1"

    >
      <v-icon dark>
        mdi-minus
      </v-icon>
    </v-btn>
  </div> 
  
</template>

<script>
export default {
  data:() => ({
   
   quantidade: 0
  
  })
}
</script>

<style>

</style>