<template>
    <div>
        <b-card 
          v-bind:title="posttitle"
        >
          <b-card-text>
            {{message}}
          </b-card-text>

          <b-button href="#" variant="primary">View More</b-button>
        </b-card>
    </div>
</template>

<script>
export default {
    name: "DataCard",
    props: {
      posttitle: String, 
      message: String
    }
}
</script>

