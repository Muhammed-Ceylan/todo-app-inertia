<template>
    <div>
        Burası Index.vue sayfasıdır.
    </div>
    <hr/>
    <ul>
        <li v-for ="article in articles" :key="article.id">
            {{ article.title }}
        </li>
    </ul>
</template>

<script>
    export default {
        props: ['articles'],
    }
</script>
