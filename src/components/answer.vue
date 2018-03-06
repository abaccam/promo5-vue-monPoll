<template>
   <section>
     <h1>* JEAN POLL *</h1>
      <form @submit.prevent="onSubmit()">
          <h2>{{poll.title}}</h2>
        <div class="form-group">
            <!-- <input type="text" :name="poll.title" :value="poll.title"> -->
            <div
                v-for="(option, index) in poll.options" 
                :key="index"  class="form-group"> 
                <label>{{option.text}}</label>
                <input type="radio"
                name="poll"
                :value="option.id"
                v-model = "picked"
                class="form-control" 
                aria-label="Radio button for following text input">
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
     picked:null,
     poll : {
        title: "Que boire au petit dej ?",
        options: [
            {id: 1, text: "Thé"},
            {id: 2,text: "Café"},
            {id: 3,text: "Jus d'orange"},
            {id: 4,text: "Rien, je suis en retard"},
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
       onSubmit(){
               console.log(this.picked);
           
       }
    }
    
}

</script>

<style>

</style>
