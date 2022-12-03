<template>
    <v-card rounded="pill" :prepend-icon="icon" class="ma-2 pa-2">
    <template v-slot:title> {{ civ }} </template>
    </v-card>
</template>
  
<script >
export default {
  props: {
    civ: String,
    icon: String
  },

  mounted() {
    console.log(this.civ)
  }
}
</script>
  