<template>
 <div class="game-bg">
    <h1>Color Picker Game</h1>

    <div>{{ message }}</div>

    <button 
      v-for="color in colors" 
      :key="color" 
      @click="matchColor(color)">
      {{ color }}
    </button>
 </div>

</template>

<script>
import ColorPicker from '../composables/ColorPicker';
export default {
  setup() {
    const {colors, message, matchColor} = ColorPicker()
    return { colors, message, matchColor };
  },
};
</script>

<style scoped>
.game-bg{
    background: #b7b713;
    padding: 1rem;
    font-size: 1.5rem;
    color: black;
    width: 600px;
    height: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 40px;
}
h1{
  border-bottom: 1px solid white;
  margin: 10px 0;
}
button{
  padding: 8px 12px;
  border-radius: 8px;

}

</style>