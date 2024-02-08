<template>
  <div class="digital-clock">
    {{ currentTime }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTime: ""
    };
  },
  mounted() {
    this.updateTime();
    setInterval(() => {
      this.updateTime();
    }, 1000);
  },
  methods: {
    updateTime() {
      this.currentTime = new Date().toLocaleTimeString();
    }
  }
};
</script>

<style>
.digital-clock {
  font-size: 24px;
  text-align: center;
  margin-top: 50px;
}
</style>
