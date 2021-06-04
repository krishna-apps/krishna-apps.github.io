<template>
  <footer>
    <div class="footer">
      <footer-info></footer-info>
      <footer-form></footer-form>
      <footer-services :serveices="$parent.svc"></footer-services>
    </div>
    <p class="copyright">
      © {{ new Date().getFullYear() }} Krishna Apps. All Rights Reserved.
    </p>
  </footer>
</template>

<script>
import FooterInfo from './FooterInfo';
import FooterForm from './FooterForm';
import FooterServices from './FooterServices';

export default {
    components: {
        FooterInfo,
        FooterForm,
        FooterServices
    }
}
</script>
