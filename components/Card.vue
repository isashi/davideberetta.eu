<template>
  <div>
    <div class="cards" :style="cssVars">
      <div class="imgBX">
        <div>
          <img :src="image" width="150">
          <h2>{{ title }}</h2>
        </div>
      </div>
      <div class="overlay"></div>
      <div class="content">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  props: ["image", "title", "description", "firstColor", "secondColor"],
  computed: {
    cssVars() {
      return {
        "--firstColor": this.firstColor,
        "--secondColor": this.secondColor
      };
    }
  }
};
</script>

<style scoped>
.cards {
  margin: 0 20px; 
  border: solid 2px rgba(255, 255, 255, 0.5);
  position: relative;
  height: 500px;
  background-color: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(45deg, var(--firstColor), var(--secondColor));
}

.cards:before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 50%;
  height: 100%;
  background: rgba(255, 255, 255, 0.1);
  z-index: 20;
  pointer-events: none;
}

.cards .imgBX {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.cards .imgBX h2 {
  margin: 10px 0 0;
  padding: 0;
  color: #fff;
  font-weight: 700;
  font-size: 150%;
  letter-spacing: 2;
  text-transform: uppercase;
}

.cards .overlay {
  position: absolute;
  bottom: 20px;
  right: 20px;
  width: 50px;
  height: 50px;
  background: #fff;
  box-shadow: 0 2px 5px rgba (0, 0, 0, 0.2);
  cursor: pointer;
  border-radius: 50%;
  transition: 0.5s;
  background: linear-gradient(45deg, var(--firstColor), var(--secondColor));
}

.cards .overlay:hover {
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  box-shadow: none;
  opacity: 0.9;
  border-radius: 0;
}

.cards .overlay:before {
  content: "Read";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  color: #fff;
  font-size: 12px;
  text-transform: uppercase;
  font-weight: 500;
  letter-spacing: 1px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition-delay: 0.5s;
}

.cards .overlay:hover:before {
  display: none;
  transition-delay: 0.5s;
}

.cards .content {
  padding: 20px;
  box-sizing: border-box;
  z-index: 1;
  pointer-events: none;
  opacity: 0;
  visibility: hidden;
  transition: 0;
  color: #fff;
}

.cards .overlay:hover ~ .content {
  opacity: 1;
  visibility: visible;
  transition: 0.3s;
  transition-delay: 0.5s;
}

.cards .content h2 {
  color: #fff;
  margin: 0;
  padding: 0;
}
</style>

