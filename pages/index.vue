<template>
  <div>
    <pre>
      {{ characters.info.pages }}
    </pre>


  </div>


</template>

<script>
import gql from 'graphql-tag'

export default {

  apollo: {
    characters: gql`
        query getCharacters {
                characters{
                  info{
                      pages
                      next
                      prev
                    }
                  }        }
    `
  }


}
</script>

<style>

</style>
