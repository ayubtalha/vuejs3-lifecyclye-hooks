<template>
  <div>
    <p>Reaction Time Score is - {{ score }} ms</p>
    <p class="rank">{{ rank }} Speed</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 500) {
      this.rank = "Impressive";
    } else if (this.score < 1000) {
      this.rank = "Good";
    } else {
      this.rank = "Too Slow ...";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
