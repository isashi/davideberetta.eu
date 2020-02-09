<template>
  <div>
    <Header></Header>
    <AboutMe></AboutMe>
    <CardSection></CardSection>
    <ContactForm></ContactForm>

    <MiniFooter></MiniFooter>
    <script data-cfasync="false" type="text/javascript" src="form-submission-handler.js"></script>
  </div>
</template>

<script>
import AboutMe from "@/components/AboutMe.vue";
import Header from "@/components/Header.vue";
import CardSection from "@/components/CardSection.vue";
import ContactForm from "@/components/ContactForm.vue";
import MiniFooter from "@/components/MiniFooter.vue";

export default {
  components: {
    AboutMe,
    Header,
    CardSection,
    ContactForm,
    MiniFooter
  }
};
</script>

<style>
.container {
  position: relative;
  width: 80%;
  display: grid;
  justify-content: space-between;
}
</style>
