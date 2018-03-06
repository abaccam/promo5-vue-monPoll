<template>

    <section>
        <h1>* JEAN POLL *</h1>
        <form @submit.prevent="onSubmit()">
          
          <div class="form-group">
            <input type="text" name="title" placeholder="Title" 
            v-model="poll.title" required>    
          </div>
          
          <div v-for="(option, index) in poll.options" 
          :key="index"  class="form-group">

            <input type="text" 
            :name="`option${index + 1}`"
            :placeholder="`Option ${index + 1}`"
            v-model="poll.options[index]" required>

            <button
            type="button"
            class="btn btn-link"
            @click="remove(index)"
            v-if="poll.options.length > 2">
              Remove
            </button>
          </div>

          <div class="form-group">
            <button
            type="button"
            class="btn btn-link"
            @click="add()">
              Add
            </button>
          </div>
          <input type="submit">
        </form>
    </section>
  
</template>

<script>
// import answer from "./answer.vue";

export default {
  name: "create",
  components: {},

  data() {
    return {
        poll:{
            title: "",
            options: ["", ""]
        }
      
    };
  },

  methods: {
    onSubmit() {
      console.log(this.poll.title, this.poll.options);
    },
    add() {
      this.poll.options.push("");
    },
    remove(index) {
      this.poll.options.splice(index, 1);
    }
  }
};
</script>

<style>

h1 {
  font-size: 50px;
}
</style>
