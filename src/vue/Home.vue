<template>
    <div>
        <b-carousel id="carousel1"
                    style="text-shadow: 1px 1px 2px #333;"
                    controls
                    indicators
                    background="#ababab"
                    :interval="3000"
                    img-width="1024"
                    img-height="480"
                    v-model="slide"
                    @sliding-start="onSlideStart"
                    @sliding-end="onSlideEnd">

            <b-carousel-slide>
                <img slot="img" class="d-block img-fluid w-100"
                     src="./../assets/img/main_01.jpg" alt="image slot">
            </b-carousel-slide>

            <b-carousel-slide>
                <img slot="img" class="d-block img-fluid w-100"
                     src="./../assets/img/main_02.jpg" alt="image slot">
            </b-carousel-slide>

            <b-carousel-slide>
                <img slot="img" class="d-block img-fluid w-100"
                     src="./../assets/img/main_03.jpg" alt="image slot">
            </b-carousel-slide>

            <b-carousel-slide>
                <img slot="img" class="d-block img-fluid w-100"
                     src="./../assets/img/main_04.jpg" alt="image slot">
            </b-carousel-slide>

        </b-carousel>

        <div>
            <div class="d-flex justify-content-between m-3">
                <h5>포트폴리오</h5>
                <a href="#/portfolio">더보기</a>
            </div>
            <div class="d-flex justify-content-between m-3" style="height: 150px">
                <img src="./../assets/img/main_01.jpg" style="width: 25%"/>
                <img src="./../assets/img/main_02.jpg" style="width: 25%"/>
                <img src="./../assets/img/main_03.jpg" style="width: 25%"/>
                <img src="./../assets/img/main_04.jpg" style="width: 25%"/>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Home',
        data () {
            return {
                slide: 0,
                sliding: null
            }
        },
        methods: {
            onSlideStart () {
                this.sliding = true
            },
            onSlideEnd () {
                this.sliding = false
            }
        }
    }
</script>