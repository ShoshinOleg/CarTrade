<template>
    <div class="vCarCatalog">
        <vHeader/>
        <hr class="py-0"> 
        <div class="container px-0">
            <div class="row no-gutters pt-3"> <!--search cars-->
                <div class="col-9">
                    <vCarSearchBlock/>
                    <div class="container px-0 mt-4"> <!--Список объявлений-->
                        <div v-for="car in cars" :key="car.id">
                            <hr>
                            <vShortCarDescription :car="car"/>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <vFooter/>
    </div>
</template>

<script>
import vHeader from "../components/vHeader"
import vCarSearchBlock from "../components/vCarSearchBlock"
import vShortCarDescription from "../components/vShortCarDescription"
import vFooter from "../components/vFooter"

export default {
    name: 'vCarCatalog',
    components: {
        vHeader,
        vCarSearchBlock,
        vShortCarDescription,
        vFooter
    },
    data() {
        return {
            cars: [
                {
                    id: 1,
                    name: "Skoda Rapid",
                    year: 2014,
                    price: 449000,
                    odometer: 740000,
                    volume: 1.6,
                    power: 102,
                    fuel: 'Бензин',
                    drivetrain: 'Передний',
                    color: 'Белый',
                    transmission: 'Механика',
                    bodyStyle: 'Седан'
                },
                {
                    id: 2,
                    name: "Skoda Rapid",
                    year: 2019,
                    price: 888000,
                    odometer: 200000,
                    volume: 1.6,
                    power: 102,
                    fuel: 'Бензин',
                    drivetrain: 'Передний',
                    color: 'Белый',
                    transmission: 'Автомат',
                    bodyStyle: 'Седан'
                },
                {
                    id: 3,
                    name: "Skoda Rapid",
                    year: 2017,
                    price: 666000,
                    odometer: 740000,
                    volume: 1.6,
                    power: 102,
                    fuel: 'Газ',
                    drivetrain: 'Передний',
                    color: 'Белый',
                    transmission: 'Механика',
                    bodyStyle: 'Седан'
                }
            ]
        }
    }
}
</script>