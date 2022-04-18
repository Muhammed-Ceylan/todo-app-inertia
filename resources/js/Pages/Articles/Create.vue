
<template>
    <AppLayout title="Create a New Article">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">  
                Create a New Article
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <form @submit.prevent="submitForm">
                        <!-- v-model ile datadaki boş alanları doldur ve forma gönder-->
                        <input type="text" name="title" placeholder="Title" v-model="form.title"/>
                        <br>
                        <textarea name="body" placeholder="Body" v-model="form.body"></textarea>
                        <br>
                        <button type="submit">Create Article</button>
                    </form>
                </div>
            </div>
        </div>
    </AppLayout>
</template>

<script>
import AppLayout from '@/Layouts/AppLayout.vue';

export default {
    components: {
        AppLayout,
    },
    methods: {
        //article içerisindeki alana pot edilecek.
        submitForm() {
            this.form.post(this.route("articles.store"));
        },
    },
    data() {
        return {
            //sgönderilen formu inertia forma dönüştürüyor.
            form: this.$inertia.form ({
                title: '',
                body: '',
            }),
        };
    },
};
</script>
