<template>
    <Head title="Bulletin Board" />

    <BreezeAuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Welcome to the Bulletin Board
            </h2>
        </template>
    </BreezeAuthenticatedLayout>
</template>

<script>

import BreezeAuthenticatedLayout from '@/Layouts/Authenticated.vue'
import { Head } from "@inertiajs/inertia-vue3";


export default {
  components: {
    Head,
    BreezeAuthenticatedLayout,
  },
};
</script>

<style>
</style>