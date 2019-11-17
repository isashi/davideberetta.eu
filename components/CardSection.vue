<template>
  <div class="card_section">
    <div class="container">
      <Card
        title="Analysis"
        description="Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova"
        image="/images/analysis.svg"
        firstColor="#3503ad"
        secondColor="#f7308c"
      ></Card>
      <Card
        title="Design"
        description="Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova"
        image="/images/design.svg"
        firstColor="#ccff00"
        secondColor="#09afff"
      ></Card>
      <Card
        title="Code"
        description="Testo di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di provaTesto di prova"
        image="/images/code.svg"
        firstColor="#e91e63"
        secondColor="#ffeb3b"
      ></Card>
    </div>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";

export default {
  components: {
    Card
  },
  data() {
    return {};
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
  background-color: #333;
}

.container {
  position: relative;
  width: 1000px;
  display: flex;
  justify-content: space-between;
}
</style>


