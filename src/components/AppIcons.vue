<script>
    export default{
        name: "AppIcons",
        data(){
            return {
                icons: [
                    {
                        src: "comics-digital-comics.png",
                        text: "digital comics"
                    },
                    {
                        src: "comics-merchandise.png",
                        text: "dc merchandise"
                    },
                    {
                        src: "comics-subscriptions.png",
                        text: "subscription"
                    },
                    {
                        src: "comics-shop-locator.png",
                        text: "comic shop locator"
                    },
                    {
                        src: "dc-power-visa.svg",
                        text: "dc power visa"
                    },
                ]
            }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/buy-${name}`, import.meta.url).href
            }
        }
    };
</script>

<template>
    <section>
        <div class="container">
            <div class="icon-card" v-for="icon in icons">
                <img :src="getImageUrl(icon.src)" alt="{{ icon.text }}">
                <span class="icon-text">{{ icon.text }}</span>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    section{
        background-color: $primary_color;
        color: white;
    }

    .container{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        align-items: center;
        height: $small_sect_h;
    }

    .icon-card{
        height: 30%;
        display: flex;
        align-items: center;
        img{
            height: 100%;
        }
        &:last-child > img{
            height: 75%;
        }
        span{
            text-transform: uppercase;
            margin-left: 6px;
        }
    }
</style>