<template>
  <div class="todo-submit">
    <b-form>
      <b-form-group
        id="input-group-1"
        label="Todo:"
        label-for="input-1"
      >
        <b-form-input
          id="input-1"
          v-bind:value = "message"
          type="text"
          required
        ></b-form-input>
      </b-form-group>
      <b-button type="button" variant="primary" v-on:click="postTodo">Submit</b-button>
    </b-form>
    <!-- <input type="text" v-model="message"> -->
    <!-- <input type="button" v-on:click="postTodo"> -->
    <ul>
        <li v-for="todo in todos">
            {{ todo }}
        </li>
    </ul>
  </div> 
</template>

<script>
export default {
  name: 'todo-submit',
  data () {
    // called every time before loading the component
    // as the name said, it can be async
    // Also, the returned object will be merged with your data object
    return { 
        message: 'message',
        todos: []
    }
  },
  methods: {
    postTodo: function() {
        this.todos.push(this.message)
        this.message = ""
    }
  }
}
</script>