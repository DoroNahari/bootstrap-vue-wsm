<template>
  <b-container fluid class="d-flex h-100 flex-column">
    <b-row>
      <b-col lg="12" xl="12">
        <b>Dev Space Name</b>
        <p>Dev spcaces > Create new</p>
      </b-col>
    </b-row>
    <b-row class="row flex-fill d-flex justify-content-start overflow-none">
      <b-col lg="4" xl="4" class="pt-3">
        <b-row>
          <b-col lg="12" xl="12">
            <b>Dev Space Name</b>
          </b-col>
          <b-col style="text-align: left;" lg="12" xl="12">
            <b-input></b-input>
          </b-col>
        </b-row>
      </b-col>
      <b-col class="pt-3" style="background: white;" lg="6" xl="6">
        <b-row>
          <b-col lg="12" xl="12">
            <h5>Dev Space Name</h5>
          </b-col>
          <b-col lg="12" xl="12">
            <h6>for SAP Fiory/SAPUI5 Applications</h6>
            <p>Develop and extend SAP Fiory and SAPUI5 applications. Quickly enable and launch new business scenarios by developing your own apps or by extending and customizing SAP Fiori applications delivered by SAP</p>
            <br>
          </b-col>
        </b-row>
        <b-row>
          <b-col lg="6" xl="6">
            <h6>SAP Predefined Extensions</h6>
            <p>The following extensions will be available by default</p>
            <b-list-group>
              <b-list-group-item v-for="item in items" :key="item">
                <b>{{item.name}}</b>
                <p>{{item.Description}}</p>
              </b-list-group-item>
            </b-list-group>
          </b-col>
          <b-col lg="6" xl="6">
            <h6>Additional SAP Extensions</h6>
            <p>Select the recommended extensions you would like to have in your dev space. You Can later add more directly from your space.</p>
            <b-list-group>
              <b-list-group-item v-for="item in items" :key="item">
                <b-row>
                  <b-col lg="2" xl="2">
                    <b-form-checkbox></b-form-checkbox>
                  </b-col>
                  <b-col lg="2" xl="2">
                    <img v-bind:src="items">
                  </b-col>
                  <b-col lg="5" xl="5">
                    <b>{{item.name}}</b>
                    <p>{{item.Description}}</p>
                  </b-col>
                </b-row>
              </b-list-group-item>
            </b-list-group>
          </b-col>
        </b-row>
      </b-col>
      <b-col style="background: white;" lg="2" xl="2"></b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      svg: "../assets/extImg.png",
      items: [
        { name: "Cds-tools", Description: "Provide cds tools", svg: "../assets/extImg.png" },
        { name: "Mta-tools", Description: "Provide mta tools", svg: "../assets/extImg.png" }
      ]
    };
  }
};
</script>

<style>
.list-group-item {
  border: none;
}
</style>
