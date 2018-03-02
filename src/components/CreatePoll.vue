<template>
  <button type="submit" value="Submit">Submit</button>
</template>

<script>
import List from './Choise.vue';
export default {
  

  name:'CreatePoll',
    components: {
        Choise
    },
    /**
     * La propriété data du component est une fonction qui return un objet
     * contenant la liste des variables que l'on souhaite rendre accessible
     * dans le template.
     */
    data: function(){
        return {
            tab: ['ga', 'zo', 'bu', 'meu', 'ga']
        }
    },
    /**
     * La propriété methods du component est un objet contenant les 
     * méthodes que l'on veut rendre accessible au template
     */
    methods: {
        show() {
            alert('kekchoz');
        },
        showItem(item) {
            console.log(item);
        },
        remove(nb){
            //Pour accèder à une variable data ou une méthode
            // de notre component, on peut utiliser le this
            this.tab.splice(nb, 1)
        }
    }
}

</script>

<style>

</style>
