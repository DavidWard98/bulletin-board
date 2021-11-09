<template>
  <Head title="Bulletin Board" />

  <BreezeAuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">
        Welcome to the Bulletin Board
      </h2>
      <BreezeLink href="/posts/create">Create Post</BreezeLink>
    </template>
  </BreezeAuthenticatedLayout>
</template>

<script>
import BreezeAuthenticatedLayout from "@/Layouts/Authenticated.vue";
import { Head } from "@inertiajs/inertia-vue3";
import BreezeLink from "@/Components/NavLink.vue";

export default {
  components: {
    Head,
    BreezeAuthenticatedLayout,
    BreezeLink,
  },
};
</script>

<style>
</style>