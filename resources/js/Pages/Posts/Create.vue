<template>
  <Head title="Bulletin Board" />

  <BreezeAuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">
        Create posts
      </h2>
    </template>

    <div>
      <form @submit.prevent="submit" method="POST" action="/">
        <breeze-label value="Title" for="title" />
        <breeze-input :modelValue="form.title" type="text" for="title" />

        <breeze-input :modelValue="form.content" type="text" for="content" />
        <breeze-button type="submit" :disabled="form.processing">
          Create
        </breeze-button>
      </form>
    </div>
  </BreezeAuthenticatedLayout>
</template>

<script>
import BreezeAuthenticatedLayout from "@/Layouts/Authenticated.vue";
import { Head } from "@inertiajs/inertia-vue3";
import BreezeLabel from "@/Components/Label.vue";
import BreezeInput from "@/Components/Input.vue";
import BreezeButton from "@/Components/Button.vue";
import { Inertia } from "@inertiajs/inertia";

export default {
  components: {
    Head,
    BreezeAuthenticatedLayout,
    BreezeLabel,
    BreezeInput,
    BreezeButton,
  },
  data() {
    return {
      form: this.$inertia.form({
        title: "",
        content: "",
      }),
    };
  },
  methods: {
    submit() {
      Inertia.post("/posts", this.form);
    },
  },
};
</script>

<style>
</style>