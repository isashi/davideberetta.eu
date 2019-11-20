<template>
  <div>
    <Header></Header>
    <CardSection></CardSection>
    <ContactForm></ContactForm>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import CardSection from "@/components/CardSection.vue";
import ContactForm from "@/components/ContactForm.vue";

export default {
  components: {
    Header,
    CardSection,
    ContactForm
  }
};
</script>

<style scoped>
</style>
