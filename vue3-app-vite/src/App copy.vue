<template>
  <p>
    <button @click="increase">count: {{ count }}</button>
  </p>
</template>

<script>
export default {
  data: () => ({
    count: 0
  }),
  methods: {
    increase() {
      console.log(this);
      this.count++;
    }
  }
}
</script>

