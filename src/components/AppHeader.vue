<script>
    export default {
        name: "AppHeader",
        data() {
            return {
                isNavOpen: false
            };
        },
        methods: {
            toggleNavbar() {
                this.isNavOpen = !this.isNavOpen;
            }
        }
    };
</script>

<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <a class="navbar-brand" href="#">
                <img src="../assets/img/dc-logo.png" alt="" srcset="">
            </a>
            <button class="navbar-toggler" type="button" @click="toggleNavbar">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse my-header" :class="{ 'show': isNavOpen }">
                <div class="navbar-nav">
                    <a class="nav-link" href="#" >CHARACTES</a>
                    <a class="nav-link" href="#">COMICS</a>
                    <a class="nav-link active" href="#">MOVIES</a>
                    <a class="nav-link" href="#">TV</a>
                    <a class="nav-link" href="#">GAMES</a>
                    <a class="nav-link" href="#">COLLECTIBLES</a>
                    <a class="nav-link" href="#">VIDEOS</a>
                    <a class="nav-link" href="#">FANS</a>
                    <a class="nav-link" href="#">NEWS</a>
                    <a class="nav-link" href="#">SHOP</a>
                    

                </div>
            </div>
        </div>
    </nav>
</template>

<style scoped lang="scss">
    @use '../assets/scss/variables' as *;

    img{
        display: block;
        max-width: 90px;
    }

    .nav-link {
            font-size: 14px;
            color: $brand-text-primary;

            &.active {
                color: $brand-primary !important;
                position: relative;
            }
    }

    @media screen and (min-width:992px) {
        .my-header {
            display: flex;
            justify-content: flex-end;
        }

        .nav-link {
            font-size: 14px;
            color: $brand-text-primary;

            &.active {
                color: $brand-primary !important;
                position: relative;
            }

            &.active::after {
                content: '';
                width: 100%;
                height: 4px;
                background-color: $brand-primary;
                position: absolute;
                left: 0;
                bottom: -31px;
            }

        }


    }
</style>
