<template>
  <div id="app">
  <div style="margin:10% 25%; width:250px">
    <br>
    <ejs-listbox :dataSource='dataItem' :fields='dataFields'
    popupHeight="200px" popupWidth="250px" sortOrder="Descending" >
    </ejs-listbox>
  </div>
  </div>
</template>

<script>
import Vue from "vue";
import {ListBoxPlugin} from "@syncfusion/ej2-vue-dropdowns";
Vue.use(ListBoxPlugin);
//import {DataManager, WebApiAdaptor} from "@syncfusion/ej2-data";
export default Vue.extend({
  data: function() {
    return {
	dataItems: [
          { Id: 'game1', Game: 'Football' },
          { Id: 'game2', Game: 'Basketball' },
          { Id: 'game3', Game: 'Volleyball' }
        ],
      dataFields: { text: 'Game', value: 'Id' },
      // dataData: new DataManager({
      //   url: 'https://ej2services.syncfusion.com/production/web-services/api/Employees',
      //   adaptor: new WebApiAdaptor,
      //   crossDomain: true
      //   }),
      // dataFields: { text: 'FirstName', value: 'EmployeeID' }
    };
  }
});
</script>

<style>
@import url(https://cdn.syncfusion.com/ej2/material.css);
</style>
