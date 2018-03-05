<template>
   <section>
     <h1>* JEAN POLL *</h1>
      <form>
        <div class="form-group">
            <input type="text" :name="poll.title" :value="poll.title">
            <div
                v-for="(option, index) in poll.options" 
                :key="index"  class="form-group"> 
                <label>{{option.text}}</label>
                <input type="radio"
                name="options"
                class="form-control" aria-label="Radio button for following text input"
                >

            </div>

            <input type="submit">
        </div>            
      </form>
   </section>  
</template>

<script>
export default {

name:'answer',
components: {},

  data() {
    return {
     poll : {
        title: "Que boire au petit dej ?",
        options: [
            {text: "Thé", checked: false},
            {text: "Café", checked: false},
            {text: "Jus d'orange", checked: false},
            {text: "Rien, je suis en retard", checked: false},
        ]
     }    
}
  
    // props: {
    //     tab: {
    //         type: Array,
    //         required: true
    //     }
  },
    methods: {
       
    }
    
}

</script>

<style>

</style>
