<script>
    export default{
        name: "AppContacts",
        data() {
            return {
                socialIcons: [
                    "facebook.png",
                    "periscope.png",
                    "pinterest.png",
                    "twitter.png",
                    "youtube.png"
                ]
            }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/footer-${name}`, import.meta.url).href
            }
        }
    };
</script>

<template>
    <section>
        <div class="container">
            <button type="button">sign-up now!</button>
            <div class="social">
                <span>follow us</span>
                <a href="#" v-for="icon in socialIcons">
                    <img :src="getImageUrl(icon)" alt="">
                </a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    section{
        background-color: $secondary_dark;
        color: white;
        height: $small_sect_h;
    }

    .container{
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 100%;
    }

    button{
        background-color: transparent;
        border: 2px solid $primary_color;
        padding: 10px;
        color: white;
        text-transform: uppercase;
        font-size: 1rem;
        cursor: pointer;
    }

    .social{
        display: flex;
        align-items: center;
        * + * {
            margin-left: 15px;
        }
        span{
            color: $primary_color;
            text-transform: uppercase;
        }
    }
</style>