<template>
  <div id="app">
       <b-navbar toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="#">{{ Title }}</b-navbar-brand>
        </b-navbar>


        <data-card
          v-for="item in items"
          v-bind:key="item.id"
          v-bind:posttitle="item.posttitle"
          v-bind:message="item.message"
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
      Title: "Demo Boi",
      items: [
        {
          id:1,
          posttitle: "HeeHee",
          message: "Let's talk about how Michael Jackson laughs"
        },
        {
          id:2,
          posttitle: "My Journey to India",
          message: "Lets talk about the land of spicy food"
        }
      ]
    }
  }
}
</script>

<style>

</style>
