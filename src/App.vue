<template>
  <div id="app">
       <b-navbar toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="#">{{ Title }}</b-navbar-brand>
        </b-navbar>

        <DataCard 
          posttitle="HeeeHeee"
          message="Wow this will be a fun one to read"
        />
  </div>
</template>

<script>
import DataCard from './components/DataTab.vue'
export default {
  name: 'app',
  components: {
    DataCard
  },
  data () {
    return {
      Title: "Demo Boi"
    }
  }
}
</script>

<style>

</style>
