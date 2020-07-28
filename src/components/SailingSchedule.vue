<template>
  <div class="sailing-schedule-container float-left">
    <div class="left-column">
      <!-- image only -->
      <img
        src="../assets/bitmap.png"
        srcset="../assets/bitmap@2x.png 2x, ../assets/bitmap@3x.png 3x"
        class="logo-image"
      />
    </div>
    <div class="right-column">
      <div class="row">
        <div class="port-name float-left">
          Jebel Ali
          <div class="port-code">AE</div>
        </div>
        <div class="port-name float-left text-right ml-6">
          Jiujang (Jianxi)
          <div class="port-code">CN</div>
        </div>
      </div>
      <div class="row mt-14">
        <!-- <i class="fas fa-anchor"></i> -->
        <img src="../assets/group-3.svg" class="port-icon" />
        <div class="origin-port-to-vessel-line"></div>
        <img src="../assets/ship.svg" class="port-icon" />
        <div class="vessel-to-destination-port-line"></div>
        <img src="../assets/group-3.svg" class="port-icon" />
      </div>
      <div class="row mt-19">
        <img src="../assets/calendar.svg" class="calendar-icon" />
        <div class="departure-date">
          <span>Estimated Departure</span>
          <br />
          <span>01 Sep 2020</span>
        </div>
        <div class="date">Non Stop</div>
        <div class="arrival-date">
          <span>Estimated Departure</span>
          <br />
          <span>01 Sep 2020</span>
        </div>
        <img src="../assets/calendar.svg" class="calendar-icon ml-8" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SailingSchedule",

  data() {
    return {};
  },

  methods: {}
};
</script>

<style>
.sailing-schedule-container {
  width: 100%;
}
.left-column {
  width: 120px;
  float: left;
  margin-left: 31px;
  margin-right: 31px;
}
.right-column {
  float: right;
  width: 450px;
}
.port-name {
  width: 206px;
  height: 36px;
  font-family: Roboto;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  letter-spacing: 0.5px;
  color: var(--black);
}
.port-code {
  line-height: 1.5;
  font-size: 10px;
  font-weight: bold;
  letter-spacing: 0.31px;
}
.port-icon {
  width: 24px;
  height: 24px;
  object-fit: contain;
}
.origin-port-to-vessel-line {
  width: 158px;
  height: 2px;
  border: 2px dashed var(--very-light-pink);
  margin-left: 8px;
  margin-right: 8px;
  margin-top: 10px;
}
.vessel-to-destination-port-line {
  width: 157px;
  height: 2px;
  border: 2px dashed var(--very-light-pink);
  margin-left: 8px;
  margin-right: 8px;
  margin-top: 10px;
}
.calendar-icon {
  width: 16px;
  height: 16px;
  object-fit: contain;
}
.departure-date {
  width: 120px;
  height: 29px;
  font-family: Roboto;
  font-size: 10px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: normal;
  color: var(--black);
  margin-left: 8px;
}
.date {
  width: 130px;
  height: 29px;
  font-family: Roboto;
  font-size: 10px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: normal;
  text-align: center;
  color: var(--black);
}
.arrival-date {
  width: 120px;
  height: 29px;
  font-family: Roboto;
  font-size: 10px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: normal;
  text-align: right;
  color: var(--black);
}
.logo-image {
  height: 30px;
  object-fit: contain;
  display: block;
  margin: 0 auto;
}
</style>
