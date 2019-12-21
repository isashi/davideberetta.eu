<template>
  <div class="card_section">
    <Card
      v-for="(card, index) in cards"
      :key="index"
      :title="card.title"
      :description="card.description"
      :image="card.image"
      :firstColor="card.firstColor"
      :secondColor="card.secondColor"
    ></Card>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";

export default {
  components: {
    Card
  },
  data() {
    return {
      cards: [
        {
          title: "Analysis",
          description:
            "Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova",
          image: "/images/analysis.svg",
          firstColor: "#3503ad",
          secondColor: "#f7308c"
        },
        {
          title: "Design",
          description:
            "Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova",
          image: "/images/design.svg",
          firstColor: "#ccff00",
          secondColor: "#09afff"
        },
        {
          title: "Code",
          description:
            "Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova",
          image: "/images/code.svg",
          firstColor: "#e91e63",
          secondColor: "#ffeb3b"
        }
      ]
    };
  }
};
</script>

<style>
h2 {
  color: white;
}
.img {
  opacity: 1;
}

.card_section {
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: linear-gradient(#000, #333);
}

.container {
  position: relative;
  width: 80%;
  display: grid;
  justify-content: space-between;
}

/* codice con Ricardo
 .container {
  display: grid;
  grid-template-columns: 33% 33% 33%;
  height: 80vh;
  margin: 10vh;
} */
</style>


