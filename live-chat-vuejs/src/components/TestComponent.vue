<template>
  <div>
    これはコンポーネントから表示されています。
    <p>{{ message }}</p>
    <p>{{ isEnabled }}</p>
    <button @click="onClick">親メソッドを実行するボタン</button>
  </div>
</template>

<script>
export default {
  props: ['message', 'isEnabled'],

  methods: {
    onClick () {
      this.$emit('toggle')
    }
  }
}
</script>

<style scoped>
p {
  font-size: 20px;
  color: red;
}
</style>