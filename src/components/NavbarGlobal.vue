<template>
    <!-- <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </div> -->
    <nav :class="{scrolling:isScrolling}">
        <a href="#" class="brand-name">
            <span class="val">Valet</span><span class="sol">Solutions</span>
        </a>

        <ul class="nav-menu" :class="{active:openNav}">
            <li class="close-icon" @click="openNav = !openNav">
                <i class="fas fa-times"></i>
            </li>


            <!-- nav item -->
            <li class="nav-item">
                <router-link to="/" class="nav-item-link">Home</router-link>
            </li>
            <!-- nav item -->
            <li class="nav-item">
                <router-link :to="{name:'Pricing'}" class="nav-item-link">Pricing</router-link>
            </li>
            <!-- nav item -->
            <li class="nav-item">
                <router-link :to="{name: 'ContactUs'}" class="nav-item-link">contact us</router-link>
            </li>
            <!-- nav item -->
            <li class="nav-item">
                <router-link :to="{name: 'Register'}" class="nav-item-link">register</router-link>
            </li>
        </ul>


        <span class="menu-icon" @click="openNav = !openNav"><i class="fas fa-bars"></i></span>
    </nav>
</template>


<script>

export default {
    data() {
        return {
            openNav: false,
            isScrolling: false
        }
    },
    mounted() {
        window.addEventListener("scroll", () => {

            if (window.scrollY > 100) {
                this.isScrolling = true;
            } else {
                this.isScrolling = false;
            }
        })
    },
}
</script>