<template>
    <div>
        <h2>Filtros Precios</h2>
        <ul>
            <li v-for="(precio,index) of precios" :key="index">{{ precio | redondear }}</li>
        </ul>
        <p>{{ fecha | acortarFecha }}</p>
    </div>
</template>

<script>
export default {
    name: 'FiltrosPrecios',

    data() {
        return {
            precios:[12999.99,89.989898, 345000.888888, 120000, 88999.000],
            precioUnico:345.992666111,
            fecha:new Date(),
        };
    },

    filters: {
        redondear(precio){
            return precio.toFixed(2);
        },
        acortarFecha(fecha){
            return fecha.toLocaleDateString();
        }
    },
};
</script>