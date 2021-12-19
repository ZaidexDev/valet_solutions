<template>
    <header @mousemove="mouseMoveAnimation" ref="mainHeader">
            <div class="row">
                <div class="col-lg-6 col-xl-5">
                    <div class="header-title-section">
                        <h1 class="title">Valet Solutions for better  social media</h1>
                        <p class="desc">Proactively coordinate quality quality vectors vis-a-vis supply chains client-centric web services.</p>
                    
                        <div class="form-box">
                            <input type="text">
                            <button class="subscribe-btn">Subscribe</button>
                        </div>
                    </div>
                </div>
            </div>

            <span class="hero-1-dots-orange" :style="moveAnimateStyle"></span>
            <span class="hero-2-laptop" :style="moveAnimateSkew"></span>
    </header>
</template>



<script>

export default {
    data() {
        return {
            moveX : 0,
            moveY : 0,
            moveAnimateStyle: {},
            moveAnimateSkew: {}
        }
    },
    methods: {
        mouseMoveAnimation(event) {
            this.moveX = (event.pageX * 0.005);
            this.moveY = (event.pageY * 0.005);

            this.moveAnimateStyle = {
                'margin-right': '-' + this.moveX + 'px',
                'margin-bottom': '-' + this.moveY + 'px'
            }

            this.moveAnimateSkew = {
                'transform': `rotateX( -${this.moveY}deg ) rotateY( -${this.moveX}deg )`
            }

            // this.$refs.headerHero1.style = this.moveX;

            // console.log(this.$refs.headerHero1.style);
        }
    }
}
</script>
