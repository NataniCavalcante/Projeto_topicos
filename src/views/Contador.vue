<template>
<div>

<v-row>
  <v-col cols= "12">
     <v-card elevation="14"
    class="mx-auto"
    max-width="300"
    
  >
    <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="200px"
    ></v-img>

    <v-card-title>
        Quantidade de pessoas: {{quantidade}}
    </v-card-title>
    </v-card>
  </v-col> 
</v-row>

<v-row>
  <v-col cols="6">
   <v-btn block color= "green"
      class="mx-2"
      dark @click="quantidade += 1">
      <v-icon >
        mdi-plus
      </v-icon>
    </v-btn>
  </v-col>


  <v-col cols="6">
     <v-btn block color="red"  
    
      class="mx-2"
      dark @click="quantidade -= 1"
    >
      <v-icon dark>
        mdi-minus
      </v-icon>
    </v-btn>
  </v-col>
</v-row>
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