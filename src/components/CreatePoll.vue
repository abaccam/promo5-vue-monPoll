<template>

    <section>
        <h1>JEAN POLL</h1>
        <div class="container-row" id="pollborder">
            <div id="poll">
                <form action="">
                <input type="text" name="title" placeholder="Title">
                <input type="text" name="option1" placeholder="Option 1">
                <input type="text" name="option2" placeholder="Option 2">
                <button type="submit" value="Submit">Submit</button>
            </form>
            </div>
            
        </div>    
    </section>
  
</template>

<script>
import List from './Choise.vue';

export default {

  name:'CreatePoll',
    components: {
        
    },
   
      data:() => ({
          poll: [
            { title:"test", option: ""},
           
        ]
      }),
    
    methods: {
      addOption(option) {
          this.poll.push(option);
      },
      removeOption(optionId) {
         this.poll = this.poll.filter(option => option.id !== optionId);
       
      }
  }
}

</script>

<style>
.container-row{
 display:flex;
 flex-direction: row;
 justify-content: center;
}
/* #pollborder{
    border: 2px solid rgb(248, 4, 4);
} */
#poll{
    /* border: 2px solid black; */
    width: 300px;
}
h1{
 font-size: 50px;
}
</style>
