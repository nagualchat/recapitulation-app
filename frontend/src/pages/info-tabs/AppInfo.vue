<template lang="pug">
  #app-info
    h3 Концепция
    p После собственной попытки составить список, а также изучения примеров, которые удалось найти в сети, создалось впечатление, что лучше всего для этого подошла бы древовидная структура, состоящая из категорий и подкатегорий. И хоть это приложение ориентировано именно на такой формат, но всё же написано таким образом, чтобы было не обязательно его строго придерживаться.
    p Например, вы можете не использовать вложенность глубже второго уровня или вообще от неё отказаться и вместо категорий создать несколько разных списков. То же касается и возможности отмечать и вычёркивать перепросмотренных людей — эти функции сугубо опциональны.

    h3 Управление с клавиатуры
    table
      tr
        td #[span.key ↓] #[span.key ↑]
        td Перемещение по списку
      tr
        td #[span.key →] #[span.key ←]
        td Свернуть/развернуть ветку
      tr
        td #[span.key Enter]
        td Добавить новый элемент
      tr
        td #[span.key Shift + Delele]
        td Удалить
      tr
        td #[span.key F2]
        td Переименовать
      tr
        td #[span.key =]
        td Добавить примечание
      tr
        td #[span.key Esc]
        td Отменить редактирование
      tr
        td #[span.key Tab] #[span.key Shift + Tab] или #[span.key Ctrl + →] #[span.key Ctrl + ←]
        td Сдвинуть вправо/влево
      tr
        td #[span.key 1] #[span.key 2] #[span.key 3] #[span.key 0]
        td Выделить цветом
      tr
        td #[span.key -]
        td Отметить выполненным

</template>

<script>
  import BookQuote from '@/components/BookQuote.vue';

  export default {
    components: {
      BookQuote,
    }
  }
</script>

<style lang="scss">
  @import '@/assets/variables.scss';

  span.key {
    background-color: #f3f3f3;
    border: 1px solid $border-hover;
    border-radius: 2px;
    padding: 0px 5px;
  }
</style>