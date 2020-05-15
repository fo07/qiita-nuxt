<template>
  <div>
    <ValidationProvider rules="required" v-slot="{ errors }">
      <v-text-field v-model="name" :error-messages="errors" label="お名前" />
    </ValidationProvider>
    <validation-provider>
      <v-text-field v-model="email" :error-messages="errors" label="メールアドレス" />
    </validation-provider>
    <validation-provider>
      <v-text-field v-model="password" :error-messages="errors" label="パスワード" />
    </validation-provider>
  </div>
</template>

<script>
import { ValidationProvider } from "vee-validate";

export default {
  components: {
    ValidationProvider
  },
  data() {
    return {
      name: "",
      email: "",
      password: "",
      errors: ""
    };
  }
};
</script>
