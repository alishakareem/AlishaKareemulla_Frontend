<template>
  <div class="container">
    <HeaderTop projectName="Covid-19 Vaccines"
      subTitle="Check out the different kinds of vaccines available for Covid-19 disease and its details" />
    <VaccineBox :vaccines="vaccines" />
  </div>
</template>

<script>
import axios from 'axios'
import HeaderTop from './components/HeaderTop.vue'
import VaccineBox from './components/VaccineBox.vue'


export default {
  name: 'App',
  components: {
    HeaderTop,
    VaccineBox
  },

  data() {
    return {
      vaccines: [],
    };

  },

  methods: {

    // promises

    async fetchVaccines() {
      axios.get('/api')
        .then((response) => {
          this.vaccines = response.data;
          console.log(response);
        })
        .catch((error) => {
          console.log(error);
        })
    }
  },
  async created() {
    this.vaccines = await this.fetchVaccines()
    console.log(this.vaccines);
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}

.container {
  max-width: 1200px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 35px;
  display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 20px;
  
}

div {
  margin-bottom: 0.5em;

}
</style>
