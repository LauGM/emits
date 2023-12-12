<template>
    <div>
        <h1>Slots</h1>
        <slot>
            <!-- aca se inyecta el parrafo del padre -->
        </slot>
        <footer>
            <slot name="pie">
                <!-- aqui se inyecta el celular -->
            </slot>
        </footer>
    </div>
</template>

<style scoped>
    footer{
        background-color: red;
    }
</style>