<template>
    <div class="w-full flex justify-center text-3xl">Filter</div>
          <div class="flex mt-4 justify-around w-full">
            <div class="w-1/4 flex justify-center px-4">
              <select
                class="border-2 w-full text-center px-8 cursor-pointer py-4 border-sky-800 rounded-xl shadow-xl appearance-none focus:outline-none"
              >
                <option selected>Select Area</option>
              </select>
            </div>
            <div class="w-1/4 flex justify-center px-4">
              <input
                :type="datetimeTypeFrom"
                @focus="datetimeTypeFrom = 'datetime-local'"
                @blur="datetimeTypeFrom = 'text'"
                placeholder="Select Date From"
                class="border-2 w-full text-center px-8 cursor-pointer py-4 border-sky-800 rounded-xl shadow-xl focus:outline-none"
              />
            </div>
            <div class="w-1/4 flex justify-center px-4">
              <input
                :type="datetimeTypeTo"
                @focus="datetimeTypeTo = 'datetime-local'"
                @blur="datetimeTypeTo = 'text'"
                placeholder="Select Date To"
                class="border-2 w-full text-center px-8 cursor-pointer py-4 border-sky-800 rounded-xl shadow-xl focus:outline-none"
              />
            </div>
            <div class="w-1/4 flex justify-center px-4">
              <button
                class="uppercase text-2xl w-full rounded-xl shadow-xl hover:shadow-sky-600/20 hover:opacity-70 text-white bg-sky-800"
              >
                View
              </button>
            </div>
          </div>
</template>

<script>
    export default {
        data() {
            return {
                datetimeTypeFrom: "text",
                datetimeTypeTo: "text",
            }
        }
    }
</script>