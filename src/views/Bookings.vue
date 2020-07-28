<template>
  <div>
    <div class="mt-48">
      <Breadcrumbs />
    </div>
    <div class="row mt-48">
      <div class="float-left main-column">
        <div class="toggle-row">
          <div class="w-255">
            <SToggle v-model="mode" :options="modeOptions" color="secondary" />
          </div>
          <div class="ml-30 float-right">
            <SInput
              v-model="form.bookingName"
              :placeholder="'Booking Name'"
              :iconName="'fa fa-pencil-alt icon'"
              :error="$v.form.bookingName.$error"
            />
          </div>
        </div>
        <div class="mt-48">
          <SCard>
            <template v-slot:content>
              <SailingSchedule />
            </template>
            <template v-slot:footer>
              <STabs>
                <STab name="Pricing Breakdown">
                  <div class="p-32">What we do</div>
                </STab>
                <STab name="Route Details &amp; Deadlines">
                  <div class="p-32">How much we do it for</div>
                </STab>
                <STab name="Demurage &amp; Detention">
                  <div class="p-32">Why we do it</div>
                </STab>
                <STab name="Terms &amp; Conditions">
                  <div class="p-32">Why we do it</div>
                </STab>
              </STabs>
            </template>
          </SCard>
        </div>
        <div class="float-left mt-48 main-column">
          <div>
            <SAccordion>
              <template v-slot:title>
                <div class="width-100">
                  <div class="float-left">
                    <span style="text-align:left">Tab Group</span>
                  </div>
                </div>
              </template>
              <template v-slot:content>
                <div>
                  <p>This is a test accordion component</p>
                  <p>
                    We will add a form here or anything acc to our requirements
                  </p>
                  <p>This is a test accordion component</p>
                  <p>
                    We will add a form here or anything acc to our requirements
                  </p>
                  <p>This is a test accordion component</p>
                  <p>
                    We will add a form here or anything acc to our requirements
                  </p>
                  <p>This is a test accordion component</p>
                  <p>
                    We will add a form here or anything acc to our requirements
                  </p>
                </div>
              </template>
            </SAccordion>
          </div>
        </div>
      </div>
      <div class="float-right sidebar">
        <SummaryCard />
      </div>
    </div>
  </div>
</template>

<script>
import Breadcrumbs from "../components/Breadcrumbs";
import SToggle from "../components/SToggle";
import SInput from "../components/SInput";
import SCard from "../components/SCard";
import STabs from "../components/STabs";
import STab from "../components/STab";
import SAccordion from "../components/SAccordion";
import SummaryCard from "../components/SummaryCard";
import SailingSchedule from "../components/SailingSchedule";
import { required } from "vuelidate/lib/validators";

export default {
  name: "Bookings",
  components: {
    Breadcrumbs,
    SToggle,
    SInput,
    SCard,
    SailingSchedule,
    STabs,
    STab,
    SAccordion,
    SummaryCard
  },
  data() {
    return {
      mode: "air",
      modeOptions: [
        { value: "air", label: "Air" },
        { value: "land", label: "Land" },
        { value: "ocean", label: "Ocean" }
      ],
      form: {
        bookingName: ""
      }
    };
  },
  validations: {
    form: {
      bookingName: { required }
    }
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
.sidebar {
  width: 475px;
}
</style>
