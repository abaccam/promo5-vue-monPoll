<template>

  <section id="barres">
    <div class="progress">
      <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
    <div class="progress">
      <div class="progress-bar" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
    <div class="progress">
     <div class="progress-bar" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
    <div class="progress">
     <div class="progress-bar" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
    <div class="progress">
      <div class="progress-bar" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
  </section>

</template>

<script>
export default {
  name: "result",
  components: {},

  data() {
    return {
        pourcent :{
          

        },
        
        poll:{
          id: 1,
          title: "Que boire au petit dej ?",
          options: [
            {id: 1, text: "Thé", count: 10},
            {id: 2, text: "Café", count: 15},
            {id: 3, text: "Jus d'orange", count: 2},
            {id: 4, text: "Rien, je suis en retard", count: 21}
          ]
        }
    } 
  },

  methods: {
    total() {
      console.log(this.poll.title, this.poll.options);
    }
  },

};
</script>

<style>
#barres{
  width: 500px;

}
</style>
