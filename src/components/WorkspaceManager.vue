<template>
  <b-container fluid class="d-flex h-100 flex-column pt-4 px-5">
    <b-row>
      <b-col offset="0" lg="10" xl="10">
        <b-row>
          <b-col lg="12" xl="12">
            <b>Dev Spaces</b>
          </b-col>
          <b-col lg="12" xl="12">
            <p>Manage and create context basd development environment</p>
          </b-col>
        </b-row>
      </b-col>
      <b-col lg="2" xl="2">
        <b-row>
          <b-col lg="6" xl="6" class="pl-0">
            <b-input style="border-radius: 40px;" placeholder="Search"></b-input>
          </b-col>
          <b-col lg="6" xl="6" class="pl-0">
            <b-button
              block
              style="border-radius: 40px;"
              @click="createWs"
              variant="primary"
            >Create Space</b-button>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row row flex-fill d-flex justify-content-start overflow-none></b-row>
    <b-table hover :items="items"></b-table>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          Status: 40,
          Name: "Doron",
          Id: "Macdonald",
          Actions: "Icon",
          a: 123,
          b: "aaa",
          c: "bbb",
          d: "Icon"
        },
        {
          Status: 40,
          Name: "Doron",
          Id: "Macdonald",
          Actions: "Icon",
          a: 123,
          b: "aaa",
          c: "bbb",
          d: "Icon"
        },
        {
          Status: 40,
          Name: "Doron",
          Id: "Macdonald",
          Actions: "Icon",
          a: 123,
          b: "aaa",
          c: "bbb",
          d: "Icon"
        },
        {
          Status: 40,
          Name: "Doron",
          Id: "Macdonald",
          Actions: "Icon",
          a: 123,
          b: "aaa",
          c: "bbb",
          d: "Icon"
        }
      ]
    };
  },
  methods: {
    createWs() {
      this.$emit("parentCreateWs");
    }
  }
};
</script>

<style>
.container-fluid {
  background: #f4f4f4;
}
.table > thead {
  display: none;
}
.table {
  background: white;
}
tr {
  background: white;
  border-bottom: 10px solid #f4f4f4;
}
</style>
