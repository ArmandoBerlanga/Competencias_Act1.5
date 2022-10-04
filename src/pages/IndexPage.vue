<script setup>
import Card from 'components/Card.vue';

let photos = [{
        id: 4,
        title: 'Un mundo de colores',
        subtitle: 'Monterrey rumbo Madrid',
        body: 'Esta foto es del vuelo que tomé de monterrey a madrid. Desde que me subí al avión todo fue muy diferente a los vuelos nacionales que he tomado toda la vida. El avión era mucho más grande, había más personas, no iba con mi familia y sobre todo el vuelo duraba 10 horas. Este fue el comienzo de una experiencia maravillosa que sigo viviendo a día de hoy. Un mundo lleno de colores por conocer.'
    },
    {
        id: 3,
        title: 'Totillita con tinto',
        subtitle: 'Cena de campeones',
        body: 'Esta foto es del primer día que estuve en madrid y fui a cenar con unas amigas a un restaurante típico de España. Decidí probar la tortilla española y un tinto de verano. Fue una explosion de sabores muy distintos si los comparo con la comida Mexicana. Una forma distinta de comer huevo pero muy rica a su vez. Todo acompañado con una bebida en base a vino (tinto de verano) que jamás había probado.'
    },
    {
        id: 2,
        title: 'Tierras lejanas',
        subtitle: 'Ejemplo sub f2',
        body: 'lorem ipsum dolor sit amet'
    },
    {
        id: 1,
        title: 'Madrid 101',
        subtitle: 'Ejemplo sub f1',
        body: 'lorem ipsum dolor sit amet'
    },
    {
        id: 5,
        title: 'Con mi amorcito',
        subtitle: 'Un viaje lleno de amor',
        body: 'lorem ipsum dolor sit amet'
    }
];
</script>

<template>
<q-page>
    <div class="title">
        Log madrileño de aventuras
    </div>
    <div id="cards">
        <Card v-for="photo in photos" :key="photo.id" v-bind="photo" />
    </div>
</q-page>
</template>

<style lang="scss" scoped>
.title{
    font-size: 2rem;
    font-weight: 600;
    text-align: center;
    color: #7C77B9;
    background-color: #f4f4f9;
    margin-bottom: 0.8rem;
    padding: 1rem 0;
}

#cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
    grid-gap: 0.8rem;
}
</style>
