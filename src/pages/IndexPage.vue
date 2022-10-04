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
        subtitle: 'MTY-MAD-AMS en solo 2 días',
        body: 'Este fue el primer viaje que tuve fuera de España. Fui a Amsterdam con mi novia y una muy buena amiga por dos días. Este viaje fue toda una locura ya que fue el segundo día después de que llegué de Monterrey. De hecho para poder llegar al vuelo no pude ni siquiera dormir en el piso que había alquilado, ya que me tuve que ir a dormir al aeropuerto. Un viaje muy pintoresco lleno de nuevas personas, arquitectura impresionante, comida deliciosa y experiencias para toda la vida.'
    },
    {
        id: 1,
        title: 'Madrid 101',
        subtitle: 'Toledo mágico',
        body: 'Un viaje muy pintoresco a Toledo, lleno de aprendizajes culturales y de hermosos paisajes. Este fue mi primer viaje a una ciudad cerca de Madrid, comparándolo sería algo así como los pueblos mágicos que estamos tan acostumbrados en Monterrey. Fue una experiencia muy acogedora y divertida de la cual pude aprender de la cultura musulmana, la arquitectura de la edad media y un poco del catolicismo. Cómo fun fact, justo esa foto me la hizo un grupo de amigos mexicanos que conocí en el viaje.'
    },
    {
        id: 5,
        title: 'Con mi amorcito',
        subtitle: 'Un viaje lleno de amor',
        body: 'Tras no haber visto a mi novia después del viaje de ámsterdam nos reencontramos en Madrid. Pasaron casi 3 semanas de no vernos y fue algo muy difícil para mi. Ya que en Monterrey estamos acostumbrados a estar a 10 minutos de distancia. Ha sido toda una experiencia aprender a adaptarse a este nuevo entorno, ya que toda mi vida había vivido en un mismo entorno sin cambios tan significativos. Los mismos lugares, las mismas personas, el mismo idioma, todo lo mismo. Pero lo he estado logrando, Madrid ahora se siente como una extensión de mi hogar cada vez más.'
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
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    grid-gap: 0.8rem;
}
</style>
