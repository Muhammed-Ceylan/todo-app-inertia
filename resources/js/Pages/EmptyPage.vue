<script>
import AppLayout from '@/Layouts/AppLayout.vue';

export default {
    components: {
        AppLayout,
    },
};
</script>

<template>
    <AppLayout title="Place Title Here">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">  
                Place Title Here
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    Place Content Here
                </div>
            </div>
        </div>
    </AppLayout>
</template>
