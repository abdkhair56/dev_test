<template>
  <div
    class="w-full h-full flex flex-col items-center justify-start bg-sky-800"
  >
    <div class="py-12 text-white flex flex-col items-center justify-center">
      <div class="text-6xl">Developer Test</div>
      <div class="text-2xl pt-4">Abdul Khair</div>
    </div>
    <div class="container h-full px-6 py-4">
      <div class="w-full justify-start flex flex-col items-center">
        <div class="py-6 w-5/6 my-4 rounded-xl shadow-xl bg-white">
          <Filter />
        </div>
        <div
          class="w-5/6 shadow-xl rounded-xl my-4 bg-white p-4 h-[70vh] border"
        >
          <BarChart
            :labels="labels"
            :datasets="hasilChart"
            class="h-full w-full"
          />
        </div>
        <div class="w-5/6 p-4 my-8 bg-white h-[70vh] rounded-xl shadow-xl">
          <Table></Table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BarChart from "./components/BarChart.vue";
import Filter from "./components/Filter.vue";
import Table from "./components/Table.vue";
export default {
  name: "App",
  data() {
    return {
      labels: [
        "DKI Jakarta",
        "Jawa Barat",
        "Kalimantan",
        "Jawa Tengah",
        "Bali",
      ],
      hasilChart: [{ data: [90, 43, 12, 43, 85], label: "Nilai" }],
    };
  },
  components: { 
    BarChart,
    Filter,
    Table
  },
};
</script>
