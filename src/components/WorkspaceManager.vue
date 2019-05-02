<template>
  <b-container fluid>
    <b-table striped hover :items="items"></b-table>
  </b-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          { Status: 40, Name: 'Dickerson', Id: 'Macdonald', Actions: 'Icon' },
          { Status: 21, Name: 'Larsen', Id: 'Shaw', Actions: 'Icon' },
          { Status: 89, Name: 'Geneva', Id: 'Wilson', Actions: 'Icon' },
          { Status: 38, Name: 'Jami', Id: 'Carney', Actions: 'Icon' }
        ]
      }
    }
  }
</script>