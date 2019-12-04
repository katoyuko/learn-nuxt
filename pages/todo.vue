<template>
  <div class="container">
      <todo-header />
      <logo />
      <todo-submit />
      <todo />
  </div>
</template>

<script>
import TodoHeader from '~/components/TodoHeader.vue'
import Logo from '~/components/Logo.vue'
import TodoSubmit from '~/components/TodoSubmit.vue'
import Todo from '~/components/Todo.vue'

export default {
  components: {
    TodoHeader,
    Logo,
    TodoSubmit,
    Todo
  }
}
</script>