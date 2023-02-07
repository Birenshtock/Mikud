<template>
    <button class="left-btn review-btn" @click="moveReview(-1)"><i class="fa-solid fa-chevron-left"></i></button>
    <div class="flex img-txt-cont">
        <img class="review-img" :src="reviewImg" alt="no" />
        <div class="review-txt">
            <h6 class="review-txt-sub">{{ reviews[i].reviewDscription }}</h6>
            <h1 class="review-txt-title">{{ reviews[i].reviewInfo }}</h1>
            <!-- {{ reviews[i] }} -->
        </div>
    </div>
    <button class="right-btn review-btn" @click="moveReview(+1)"><i class="fa-solid fa-chevron-right"></i></button>
</template>
<script>
export default {
    components: {},
    data() {
        return {};
    },
    created() { },
    methods: {},
    computed: {},
    unmounted() { },
};
</script>
<style>

</style>