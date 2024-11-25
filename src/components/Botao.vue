<template>
  <div
    class="botao"
    :style="{ backgroundColor: color || '#666' }"
    @mousedown="pressed = true"
    @mouseup="pressed = false"
    :class="{ active: pressed }"
  >
    {{ label }}
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: '#666',
    },
  },
  data() {
    return {
      pressed: false,
    };
  },
};
</script>

<style scoped>
.botao {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  font-weight: bold;
  color: white;
  margin: 5px;
  box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.5), -4px -4px 10px rgba(255, 255, 255, 0.1);
  transition: all 0.2s;
  cursor: pointer;
}

.botao:hover {
  transform: scale(1.1);
}

.botao.active {
  transform: scale(0.9);
  box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.5);
}
</style>
