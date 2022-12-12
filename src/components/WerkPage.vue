<template>
  <div class="col-lg-6 offset-lg-3">
    <div class="accordion-item">
      <h2 class="accordion-header" :id="'flush-heading' + experience.id">
        <button
          @click="checkEven(experience.id)"
          :class="[experience.bgTest ? evenColor : unevenColor]"
          class="accordion-button collapsed"
          type="button"
          data-bs-toggle="collapse"
          :data-bs-target="'#flush-collapse' + experience.id"
          aria-expanded="false"
          :aria-controls="'flush-collapse' + experience.id"
        >
          {{ experience.work }}
        </button>
      </h2>
      <div
        :id="'flush-collapse' + experience.id"
        class="accordion-collapse collapse"
        :aria-labelledby="'flush-heading' + experience.id"
        data-bs-parent="#accordionFlushExample"
      >
        <div class="accordion-body">
          <p>
            <strong> Start date :</strong> {{ experience.startDate }}
            <strong>location :</strong>
            {{ experience.location }}
          </p>

          <p>
            {{ experience.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WerkPage",
  props: {
    experience: Object,
  },
  data() {
    return {
      startColor: "bg-secondary",
      evenColor: "bg-primary",
      unevenColor: "bg-danger",
    };
  },
  methods: {
    checkEven() {
      if (Number(this.experience.id) % 2 === 0) {
        this.startColor = this.evenColor;
      } else {
        this.startColor = this.unevenColor;
      }
    },
  },
};
</script>
