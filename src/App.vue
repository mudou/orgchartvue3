<template>
  <div id="app"><org-chart :datasource="ds"></org-chart></div>
</template>

<script>
import OrgChart from "vue-organization-chart";
import "vue-organization-chart/dist/orgchart.css";

export default {
  name: "App",
  components: {
    OrgChart
  },
  data() {
    return {
      ds: {
        id: "1",
        name: "Lao Lao",
        title: "general manager",
        children: [
          { id: "2", name: "Bo Miao", title: "department manager" },
          {
            id: "3",
            name: "Su Miao",
            title: "department manager",
            children: [
              { id: "4", name: "Tie Hua", title: "senior engineer" },
              {
                id: "5",
                name: "Hei Hei",
                title: "senior engineer",
                children: [
                  { id: "6", name: "Pang Pang", title: "engineer" },
                  { id: "7", name: "Xiang Xiang", title: "UE engineer" }
                ]
              }
            ]
          },
          { id: "8", name: "Hong Miao", title: "department manager" },
          { id: "9", name: "Chun Miao", title: "department manager" }
        ]
      }
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
