<template>
  <div class="summary-card">
    <div class="shipment-heading width-100 p-x-48">
      <div class="float-left">
        <span>Shipment Summary</span>
        <br />
        <span class="booking-name-text">Booking Name</span>
      </div>
      <div class="float-right">
        <img src="../assets/ship.svg" class="ship-icon" />
      </div>
    </div>
    <div class="float-left width-100 mt-24 p-x-48">
      <div class="float-left">
        <img src="../assets/location.svg" class="location-icon" />
      </div>
      <div class="float-left inner-heading ml-16">
        <span class="bold">ORIGIN</span>
        <br />
        <span>JEBEL ALI, AE</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 border-bottom p-x-48 p-b-24">
      <div class="float-left">
        <img src="../assets/calendar.svg" class="summary-calendar-icon" />
      </div>
      <div class="float-left inner-heading ml-16">
        <span>Estimated Arrival:</span>
        <span class="bold">01 Sep 2020</span>
        <br />
        <span>Customs clearance required</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 p-x-48">
      <div class="float-left">
        <img src="../assets/location.svg" class="location-icon" />
      </div>
      <div class="float-left inner-heading ml-16">
        <span class="bold">DESTINATION</span>
        <br />
        <span>JEBEL ALI, AE</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 border-bottom p-x-48 p-b-24">
      <div class="float-left">
        <img src="../assets/calendar.svg" class="summary-calendar-icon" />
      </div>
      <div class="float-left inner-heading ml-16">
        <span>Estimated Arrival:</span>
        <span class="bold">01 Sep 2020</span>
        <br />
        <span>Customs clearance required</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 border-bottom p-x-48 p-b-24">
      <div class="float-left">
        <img src="../assets/location.svg" class="location-icon" />
      </div>
      <div class="float-left inner-heading ml-16">
        <span class="bold">20ft</span>
        <br />
        <span>Dry Container</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 p-x-48">
      <div class="float-left width-100 total-price">
        <span class="bold">Total Price</span>
        <br />
        <span>Including Basic Freight*</span>
      </div>
      <div class="float-left total-price-number mt-8">
        <span>2,000</span>
        <span class="currency">AED</span>
      </div>
    </div>
    <div class="float-left width-100 mt-24 p-x-48">
      <SButton :label="'Confirm Booking'" :onClick="confirmBooking" />
      <span class="terms-conditions">*Terms &amp; Conditions Apply</span>
    </div>
  </div>
</template>

<script>
import SButton from "../components/SButton";
export default {
  name: "SummaryCard",

  data() {
    return {};
  },

  methods: {
    confirmBooking() {
      // console.log("CONFIRM");
    }
  },
  components: {
    SButton
  }
};
</script>

<style>
.summary-card {
  width: 348px;
  box-shadow: 0 0 50px 0 var(--very-light-pink);
  background-color: #ffffff;
  float: right;
  padding: 48px 0px;
}
.shipment-heading {
  font-family: Roboto;
  font-size: 18px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: var(--black);
}
.booking-name-text {
  font-size: 12px;
  font-weight: normal;
}
.ship-icon {
  width: 36px;
  height: 36px;
  object-fit: contain;
}
.location-icon {
  width: 24px;
  height: 24px;
  object-fit: contain;
}
.inner-heading {
  font-family: Roboto;
  font-size: 12px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.17;
  letter-spacing: 0.38px;
  color: var(--black);
}
.summary-calendar-icon {
  width: 24px;
  height: 24px;
  object-fit: contain;
}
.border-bottom {
  border-bottom: 1px solid var(--very-light-pink);
}
.total-price {
  font-family: Roboto;
  font-size: 10px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  letter-spacing: 0.31px;
  color: var(--black);
}
.total-price-number {
  font-family: Roboto;
  font-size: 36px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: var(--black);
}
.currency {
  font-family: Roboto;
  font-size: 10px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.31px;
  color: var(--black);
}
.terms-conditions {
  width: 252px;
  height: 24px;
  font-family: Roboto;
  font-size: 8px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.75;
  letter-spacing: 0.25px;
  color: var(--black);
}
</style>
