<template>
    <div>
        <div class="card-img">
            <img :src="url" :alt="title">
        </div>
        <div class="text-card"> {{ title }}</div>
    </div>
</template>

<script>
export default {
    name: 'Cards',
    props: {
        url: String,
        title: String,
    }
};
</script>

<style scoped lang="scss">

   .card-img {
        height: 155px;
        img {
            object-fit: cover;
            object-position: top;
            width: 100%;
            height: 100%;
        }
        
    }
    
    .text-card {
        color: #fff;
        font-size: 0.75rem;
        margin-top: 1rem;
        font-weight: 300;
    }

</style>