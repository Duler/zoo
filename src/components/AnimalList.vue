
<template>
  <div :id="animals" >
  <table style="width:100%">
    <tr>
      <th>Species</th>
      <th>Name</th>
      <th>Date of birth</th>
    </tr>
    <tr v-for="(animal, index) in animals" :key="index">
      <td>{{animal.species}}</td>
      <td>{{animal.name}}</td>
      <td>{{animal.dateOfBirth}}</td>
      <td>{{animal.dateOfBirth === '' ? 'Unknown' : animal.dateOfBirth}}</td>
      <td><button style="width:100%" @click="removeAnimal(index)">Remove!</button></td>
      <td><button style="width:100%" @click="moveToTop(animal, index)">moveToTop!</button></td>
    </tr>
  
  
  </table> 
  </div>
</template>
<script>
export default {
  data() {
    return {
      animals:
      [
        {species: 'Hawk', name: 'SokoStark', dateOfBirth: '12.12.1992'},
        {species: 'Fish', name: 'Vanda', dateOfBirth: '12.05.2016'},
        {species: 'Lion', name: 'Leo', dateOfBirth: '22.08.1990'},        
        {species: 'Dog', name: 'Zuca', dateOfBirth: ''},
        {species: 'Parrot', name: 'Ara', dateOfBirth: '25.01.2010'}
      ]
    }
  },
  methods: {
      removeAnimal(index) {
        this.animals.splice(index, 1);        
      },
      moveToTop(animal , index) {
        this.animals.splice(index, 1);
        this.animals.unshift(animal)
      },
    },
  
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
table, th, td {
  border: 1px solid black;
}
</style>