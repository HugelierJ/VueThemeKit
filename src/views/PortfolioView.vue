<template>
  <div class="portfolio">
    <h1>This is a portfolio page</h1>
    <div class="accordion accordion-flush" id="accordionFlushExample">
      <WerkPage
        v-for="experience in experiences"
        :key="experience.id"
        :experience="experience"
      />
    </div>
  </div>
</template>

<script>
import WerkPage from "@/components/WerkPage";

export default {
  name: "PortfolioView",
  data() {
    return {
      experiences: [
        {
          id: 1,
          work: "Builder",
          description:
            " Lorem ipsum dolor sit amet, consectetur adipisicing elit. A ad deleniti dolore doloribus eos eveniet expedita ipsam quisquam sequi voluptate?",
          location: "Kortrijk",
          startDate: "July 16, 2021",
          bgTest: false,
        },
        {
          id: 2,
          work: "Azerty",
          description:
            " Lorem ipsum dolor sit amet, consectetur adipisicing elit. A ad deleniti dolore doloribus eos eveniet expedita ipsam quisquam sequi voluptate?",
          location: "Heule",
          startDate: "August 9, 2009",
          bgTest: false,
        },
        {
          id: 3,
          work: "Qwerty",
          description:
            " Lorem ipsum dolor sit amet, consectetur adipisicing elit. A ad deleniti dolore doloribus eos eveniet expedita ipsam quisquam sequi voluptate?",
          location: "Heule",
          startDate: "August 9, 2012",
          bgTest: false,
        },
        {
          id: 4,
          work: "Lorem",
          description:
            " Lorem ipsum dolor sit amet, consectetur adipisicing elit. A ad deleniti dolore doloribus eos eveniet expedita ipsam quisquam sequi voluptate?",
          location: "Heule",
          startDate: "August 9, 2019",
          bgTest: false,
        },
      ],
    };
  },
  components: {
    WerkPage,
  },
};
</script>
