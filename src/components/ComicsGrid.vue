<script>
    import jsonData from '../dc-comics.json';

    export default{
        name: "ComicsGrid",
        data() {
            return {
                data: jsonData
            };
        }
    }
</script>

<template>
    <div class=" p-5  my-section d-flex flex-column align-items-center justify-content-center">
        <div class="d-flex align-items-center justify-content-center">
            <div class="container row d-flex ">
                <div class="col-2 " v-for="comic in data">
                    <div class="comics-container ">
                        <img :src="comic.thumb" alt="">
                    </div>
                    <p class="text-white m-2">{{ comic.series.toUpperCase() }}</p>
                </div>

            </div>
        </div>
        <button class="btn btn-primary mx-auto">LOAD MORE</button>
    </div>


</template>

<style scoped>
    .my-section{
        background-color: #1C1C1C;
    }

    .comics-container {
        width: 140px; 
        height: 140px; 
        overflow: hidden;
    }
    img {
        width: 100%; 
        height: 100%;
        object-fit: cover; 
        object-position: top;
    }
</style>
