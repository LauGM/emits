<template>
    <div class="card p-3" style="width:18rem;">
        <h5>{{ frase }}</h5>
        <div class="d-flex justify-content-center">
            <button class="btn btn-dark btn-sm" style="width:150px;">🧡</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardFrase',
    props: {
        frase:String,
    },
};
</script>

<style scoped>
    
</style>