<template>
  <div>
    <Header></Header>
    <CardSection></CardSection>
    <ContactForm></ContactForm>

    <MiniFooter></MiniFooter>
    <script data-cfasync="false" type="text/javascript" src="form-submission-handler.js"></script>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import CardSection from "@/components/CardSection.vue";
import ContactForm from "@/components/ContactForm.vue";
import MiniFooter from "@/components/MiniFooter.vue"

export default {
  components: {
    Header,
    CardSection,
    ContactForm,
    MiniFooter
  }
};
</script>

<style scoped>
</style>
