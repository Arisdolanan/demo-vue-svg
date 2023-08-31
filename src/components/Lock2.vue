<template>
  <div id="wrapper" ref="wrapper">
    <svg viewBox="0 -135 100 135" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" @click="toggleLock">
      <g id="lock" :class="{ 'lock-open': isOpen }" fill="currentColor">
        <g id="lock-body">
          <path d="M0,0 h100 v-65 l-10, -10 h-80 l-10, 10z" />
        </g>
        <g id="lock-shackle">
          <path d="M10,-75 v-30 q 0,-30,30,-30 h20 q 30,0,30,30 v30 h-15 v-30 q 0,-15,-15,-15 h-20 q -15,0,-15,15 v30z" />
        </g>
      </g>
    </svg>

  </div>
</template>
<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleLock() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>
<style>
#wrapper {
  width: 40px;
  padding: 30px;
  resize: horizontal;
  background: white;
}

svg:hover {
  cursor: pointer;
}

svg { overflow: visible; }

#lock-shackle {
  transform: rotateY(0);
  transition: transform .5s ease-in-out;
  transform-origin: 82.5px top;
}

.lock-open #lock-shackle { transform: rotateY(.5turn); }


</style>