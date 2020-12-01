<template>
    <b-container class="py-4 px-0">
        <b-carousel
        indicators
        controls
        no-wrap
        >
            <b-carousel-slide>
                <template slot="img">
                    <b-row>
                        <vCard :car="cars[0]"/>
                        <vCard :car="cars[1]"/>
                        <vCard :car="cars[0]"/>
                    </b-row>
                </template>
            </b-carousel-slide>
            <b-carousel-slide>
                <template slot="img">
                    <b-row>
                        <vCard :car="cars[0]"/>
                        <vCard :car="cars[1]"/>
                        <vCard :car="cars[0]"/>
                    </b-row>
                </template>
            </b-carousel-slide>
        </b-carousel>
    </b-container>
</template>

<script>
import vCard from "./vCard"

export default {
    name: "vCarsCarousel",
    components: {
        vCard
    },
    props: [
        'cars'
    ],

}
</script>

<style>
    .carousel-indicators li {
        background-color: black;
    }
</style>