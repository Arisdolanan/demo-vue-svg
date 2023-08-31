<template>
  <div class="svg-container">
    <svg id="en3MJP8AwCF1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 24 24" shape-rendering="geometricPrecision" text-rendering="geometricPrecision"       :class="{ unlock: unlocked }"
      @click="toggleUnlock">
      <g transform="translate(-.038159 1.058698)">
        <path d="M16.3579,10.9423l.694.055c.96811.07747,1.75845.80549,1.915,1.764.36162,2.20863.36162,4.46137,0,6.67-.15655.95851-.94689,1.68653-1.915,1.764l-1.496.12c-2.362.188-4.736.188-7.098,0l-1.496-.12c-.96843-.07758-1.75886-.8061-1.915-1.765-.3616-2.20863-.3616-4.46137,0-6.67.15655-.95851.94689-1.68653,1.915-1.764l.694-.055l8.702.001ZM12,18.31922c1.22371,0,2.21572-.9652,2.21572-2.15584s-.99201-2.15584-2.21572-2.15584-2.21572.9652-2.21572,2.15584.99201,2.15584,2.21572,2.15584Z" transform="translate(.031251 0.000001)" clip-rule="evenodd" fill-rule="evenodd"/>
      </g>
      <path class="shackle" d="M7.707151,8.795767L7.30615,6.23182v.001c-.04041-.36388-.04041-.73112,0-1.095l.023-.205c.26553-2.37923,2.27699-4.17869,4.671-4.17869s4.40547,1.79946,4.671,4.17869l.023.205c.04001.3639.04001.7311,0,1.095l-.33625,4.7q-.44015.00485-1.61389.00849q0-.00849.44853-4.30553c.02657-.20187.04038-.40894.04038-.61993c0-.09835-.003-.19584-.00889-.29235.00159-.14042-.00537-.2809-.02087-.42068l-.023-.205c-.0941-.84775-.51603-1.59416-1.1373-2.10986-.54816-.53835-1.2455-.86067-2.00469-.86067-.61036,0-1.18074.20833-1.66577.56977-.12576.07432-.24697.15759-.36265.24951-.66713.5301-1.09529,1.30439-1.18959,2.15126l-.023.205c-.0282.25389-.0282.51011,0,.764l.424199,2.728937h-1.514208Z" transform="translate(-.02-.000007)" clip-rule="evenodd" fill-rule="evenodd"/>    
    </svg>
  </div>
</template>

<script>
export default {
  data() {
    return {
      unlocked: false,
      shackleColor: "#FFFFFF", // Change this to the desired shackle color
    };
  },
  methods: {
    toggleUnlock() {
      this.unlocked = !this.unlocked;
    },
  },
};
</script>

<style scoped>
.svg-container {
  width: 100px;
  perspective: 1000px;
}

.shackle {
  stroke: #000;
  transform-origin: right;
  transition: all 0.3s ease;
  transform: translateY(12%);
}

.unlock .shackle {
  transform: translateY(2.2%);
}
</style>