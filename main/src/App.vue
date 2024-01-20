<template>
  <div>
    <input v-model="inputText" type="text" placeholder="Введите текст">
    <button @click="addItem">Добавить</button>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      items: []
    };
  },
  methods: {
    addItem() {
      if (this.inputText !== '') {

        // this.items.push(this.inputText); -- в начало списка
        // this.items.unshift(this.inputText) -- в конец списка

        // Евгений Денисович, просто откомментируйте одну из строчек, чтобы увидеть результат

        this.inputText = '';
      }
    } 
  }
};
</script>
