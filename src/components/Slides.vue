<template>
  <div class="slides_spacing"></div>
  <div class="slides">
    <transition name="slide">
      <slide
        :slide="slides[slide_ind]"
        :key="slide_ind"
      ></slide>
    </transition>
  </div>
</template>
<script>
import Slide from './Slide';
const slides = [
  {
    title: 'Business Consulting',
    description:
      'We have partnered with Dr. Vivek Bindra and Bada Business to empower youth, small businesses, MSMEs and SMEs with the most affordable and high quality entrepreneurial Skills & Knowledge.',
    images: ['/assets/vb.jpg', '/assets/vb1.jpg', '/assets/vb2.jpg'],
  },
  {
    title: '100% Customer Satisfaction',
    description:
      'We put customer satisfaction at highest priority and thanks to all our wonderful customers that we are able to maintain 100% 5✯ rating on Upwork so far!',
    images: [
      '/assets/cs.jpg',
      '/assets/cs.svg',
      '/assets/cs1.jpg',
      '/assets/cs2.jpg',
    ],
  },
  {
    title: 'Mobile And Web Development',
    description:
      'We deliver high quality Apps, Websites, Softwares and Scripts. Thanks to all our wonderful customers that we are able to maintain 100% 5✯ rating on Upwork so far!',
    images: ['/assets/m.jpg', '/assets/m1.jpg', '/assets/m1.png'],
  },
];

export default {
  name: 'Slides',
  data() {
    return {
      slides,
      slide_ind: 0,
    };
  },
  mounted() {
    setInterval(() => {
      this.slide_ind = (this.slide_ind + 1) % this.slides.length;
    }, 3500);
  },
  components: {
    Slide,
  },
};
</script>
