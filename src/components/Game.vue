<template>
    <div class="card">
        <h3>{{ title }}</h3>
        <p>{{ plateforme }}</p>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
        },
        plateforme: {
            type: String,
        },
    },
};
</script>

<style lang="scss" scoped>

</style>
