<template>
  <v-app>
    <v-main>
      <v-container >
        <v-responsive class="d-flex align-center text-center fill-height">
          <v-autocomplete
            rounded
            v-bind="this.selectedCiv"
            label="Search civ"
            :items="civs"
            item-title="name"
            item-value="name"
          ></v-autocomplete>
            <v-row align="center" justify="center" no-gutters cols="12" >
              <div v-for="civ in this.civs" :key="civ.name">
                <CivCard :civ="civ.name" :icon="civ.icon" />
            </div>
              </v-row>
        </v-responsive>
      </v-container>
    </v-main>
  </v-app>
</template>



<script>
import CivCard from "@/components/CivCard.vue";

export default {
  components: {
    CivCard,
  },

  data() {
    return {
      selectedCiv: "",
      civs: [
        { name: "Franks", icon: "FranksIcon" },
        { name: "Mayans", icon: "MayansIcon" },
        { name: "Berbers", icon: "BerbersIcon" },
        { name: "Saracens", icon: "SaracensIcon" },
        { name: "Hindustanis", icon: "HindustanisIcon" },
        { name: "Koreans", icon: "KoreansIcon" },
        { name: "Britons", icon: "BritonsIcon" },
        { name: "Magyars", icon: "MagyarsIcon" },
        { name: "Teutons", icon: "TeutonsIcon" },
        { name: "Celts", icon: "CeltsIcon" },
      ],
    };
  },

  // methods: {
  //   getImage(imagePath) {
  //     return require(imagePath);
  //   },
  // }
};
</script>