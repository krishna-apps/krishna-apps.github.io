<template>
  <div class="home">
    <nav-bar></nav-bar>
    <slides></slides>
    <services :services="svc"></services>
    <Footer></Footer>
    <modal v-model:show-modal="$root.showModal"></modal>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar';
import Slides from '@/components/Slides';
import Modal from '@/components/Modal';
import Services from '@/components/Services';
import Footer from '@/components/Footer';
export default {
  name: 'Home',
  components: {
    NavBar,
    Slides,
    Modal,
    Services,
    Footer
  },
  data() {
    return {
      svc: [
        {
          title: 'Graphics Design & Website',
          img: '/assets/graphics.gif',
          details: [
            'Graphics with your brand logo',
            'Presense on Google Map',
            'Delight Your Customers',
          ],
          bg: '#1F75A0',
        },
        {
          title: 'Mobile App Developement',
          img: '/assets/mobile.gif',
          details: [
            'Android app befitting your brand ',
            'Troubleshooting and Debugging',
            'App Maintanance ',
          ],
          bg: '#fff',
        },
        {
          title: 'Computer Vision And Analytics',
          img: '/assets/cv1.gif',
          details: [
            'Awesome Computer vision projects',
            'some other stuff',
            'some other stuff',
            'bla bla bla',
          ],
          bg: '#ddd',
        },
        {
          title: 'Business Consulting',
          img: '/assets/vb.jpg',
          details: [
            'Awesome Computer vision projects',
            'some other stuff',
            'some other stuff',
            'bla bla bla',
          ],
          bg: '#fff',
        },
        {
          title: 'Custom Solutions',
          img: '/assets/custom-cloud.gif',
          details: [
            'Awesome Computer vision projects',
            'some other stuff',
            'some other stuff',
            'bla bla bla',
          ],
          bg: '#4279E8',
        },
      ],
    };
  },
};
</script>
