<script setup>
import {
    ref
} from 'vue';

const props = defineProps({
    id: Number,
    title: String,
    subtitle: String,
    body: String
})

const counter = ref(0);
</script>

<template>
<q-card>
    <img :src="require(`assets/IMG_${id}.jpeg`)" alt="img" style="border-radius: 5%">

    <div class="info">
        <div class="title">{{ title }}</div>
        <div class="subtitle">{{ subtitle }}</div>

        <div class="line"></div>

        <div class="body">
            {{ body }}
        </div>
    </div>

    <div class="fav">
        <q-btn
            round
            color="primary"
            icon="favorite"
            size="0.8rem"
            @click="counter++" />
        <div class="counter" v-if="counter">{{ counter }}</div>
    </div>
</q-card>
</template>

<style lang="scss" scoped>
.q-card {
    display: flex;
    flex-direction: row;
    gap: 0.5rem;
    padding: 1rem;
    border-radius: 0.5rem;
    width: 100%;
    background-color: #f4f4f9;
}

img {
    width: 11.5rem;
    height: 18rem;
    object-fit: cover;
}

.info {
    display: grid;
    grid-template-rows: repeat(auto, 4);

    .title {
        font-size: 1.5rem;
        font-weight: 600;
        color: #000;
        line-height: 1.5rem;
        margin-top: 1rem;
    }

    .subtitle {
        font-size: 1rem;
        font-weight: 400;
        color: rgba(0, 0, 0, 0.521);
        line-height: 1rem;
        margin-top: 0.5rem;
    }

    .line {
        width: 100%;
        height: 2px;
        background-color: #7c77b970;
        margin: 0.5rem 0;
    }
}

.fav {
    position: absolute;
    top: 1rem;
    right: 1rem;

    .counter {
        background-color: rgb(181, 5, 5);
        color: #fff;
        border-radius: 100%;
        width: 1.25rem;
        height: 1.25rem;

        font-size: 0.7rem;
        font-weight: 600;
        text-align: center;
        line-height: 1.2rem;

        position: relative;
        top: -2.9rem;
        left: 1.5rem;
    }
}
</style>
