<template>
  <div
    class="overflow-auto whitespace-nowrap aspect-video flex flex-col flex-wrap h-[1000px] w-full"
    ref="imageGallery"
  >
    <div
      v-for="(image, index) in images"
      :key="index"
      class="h-full"
    >
      <img
        class="h-full"
        :src="image.src"
        :alt="image.alt"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { src: 'src/assets/images/image-1.jpg', alt: 'Image 1' },
        { src: 'src/assets/images/image-2.jpg', alt: 'Image 2' },
        { src: 'src/assets/images/image-3.jpg', alt: 'Image 3' },
        { src: 'src/assets/images/image-4.jpg', alt: 'Image 4' },
      ],
    };
  },
  methods: {
    handleScroll() {
      const gallery = this.$refs.imageGallery;

      if (gallery.scrollLeft + gallery.clientHeight >= gallery.scrollHeight) {
        this.images = [...this.images, ...this.getMoreImages()];
      }
    },
    getMoreImages() {
      return this.images.map((image) => ({ ...image }));
    },
  },
};
</script>
