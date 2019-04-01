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

        <b-navbar toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="#">{{ Title2 }}</b-navbar-brand>
        </b-navbar>

        <Display />
        <Sender />



  </div>
</template>

<script>
import DataCard from './components/DataTab.vue'
import Sender from './components/Sender.vue'
import Display from './components/Display.vue'

export default {
  name: 'app',
  components: {
    DataCard,
    Sender,
    Display
  },
  data () {
    return {
      Title: "Demo Part 1",
      Title2: "Demo Part 2",
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
