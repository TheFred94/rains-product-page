<template>
  <div
    class="overflow-auto whitespace-nowrap aspect-video flex flex-col flex-wrap h-[1000px] w-full keen-slider"
    ref="container"
  >
    <div
      class="keen-slider__slide"
      v-for="(image, index) in images"
      :key="index"
    >
      <img class="h-full w-full" :src="image.src" :alt="image.alt" />
    </div>
    <!--TODO Insert navigational arrows-->
  </div>
</template>
<script>
import { ref } from "vue";
import "keen-slider/keen-slider.min.css";
import { useKeenSlider } from "keen-slider/vue.js";

const animation = { duration: 60000, easing: (t) => t };

export default {
  setup() {
    const [container] = useKeenSlider({
      loop: true,
      mode: "free",
      // renderMode: "performance",
      drag: true,
      slides: {
        perView: 1,
      },
      created(s) {
        s.moveToIdx(5, true, animation);
      },
      updated(s) {
        s.moveToIdx(s.track.details.abs + 5, true, animation);
      },
      animationEnded(s) {
        s.moveToIdx(s.track.details.abs + 5, true, animation);
      },
    });
    return { container };
  },

  data() {
    return {
      images: [
        { src: "src/assets/images/image-1.jpg", alt: "Image 1" },
        { src: "src/assets/images/image-2.jpg", alt: "Image 2" },
        { src: "src/assets/images/image-3.jpg", alt: "Image 3" },
        { src: "src/assets/images/image-4.jpg", alt: "Image 4" },
      ],
    };
  },
};
</script>

<style>
@import url("keen-slider/keen-slider.css");
</style>
