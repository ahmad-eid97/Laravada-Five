<template>
  <div class="home">
    <app-login-heading></app-login-heading>
    <app-login-form></app-login-form>
  </div>
</template>

<script>
import AppLoginForm from "../../components/login/AppLoginForm.vue";
import AppLoginHeading from "../../components/login/AppLoginHeading.vue";
export default {
  middleware: ["guest"],
  name: "Login",
  components: { AppLoginHeading, AppLoginForm },
};
</script>

<style></style>
