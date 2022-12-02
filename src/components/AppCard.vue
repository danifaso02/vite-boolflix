<script>
// import CountryFlag from "vue-country-flag-next";

export default {
    name: "AppCard",
    props: {
        info: Object,
    },
    // components: {
    //     CountryFlag,
    // },
};
</script>

<template>
    <div>
        <h2>{{ info.title }}</h2>
        <h3>{{ info.original_title }}</h3>
        <div>{{ info.original_lenguage }}</div>
        <div>{{ info.vote_average }}</div>
        <!-- <div>
            <CountryFlag :country="info.original_lenguage" size="small" />
        </div> -->
    </div>
</template>

<style></style>