<template>
  <div>
    <div class="mt-48">
      <Breadcrumbs />
    </div>
    <div>
      <div class="main-column">
        <div class="toggle-row mt-48">
          <div class="w-255">
            <SToggle v-model="mode" :options="modeOptions" color="secondary" />
          </div>
          <div class="ml-30 float-right">
            <SInput
              v-model="bookingName"
              :placeholder="'Booking Name'"
              :iconName="'fa fa-pencil-alt icon'"
            />
          </div>
        </div>
        <div class="mt-48">
          <SCard>
            <template v-slot:content>
              <SailingSchedule />
            </template>
          </SCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Breadcrumbs from "../components/Breadcrumbs";
import SToggle from "../components/SToggle";
import SInput from "../components/SInput";
import SCard from "../components/SCard";
import SailingSchedule from "../components/SailingSchedule";
export default {
  name: "Bookings",
  components: {
    Breadcrumbs,
    SToggle,
    SInput,
    SCard,
    SailingSchedule
  },
  data() {
    return {
      mode: "air",
      modeOptions: [
        { value: "air", label: "Air" },
        { value: "land", label: "Land" },
        { value: "ocean", label: "Ocean" }
      ],
      bookingName: ""
    };
  },
  methods: {}
};
</script>
<style>
.toggle-row {
  display: flex;
  flex-wrap: wrap;
}
.main-column {
  width: 635px;
}
.w-255 {
  width: 255px;
}
</style>