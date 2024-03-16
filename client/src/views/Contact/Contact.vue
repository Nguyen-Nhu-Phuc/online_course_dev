<template>
    <div class="grid">
        <div class="row no-gutters">
            <div class="col lg-12 md-12 col-12">
                <div class="contact__intro-img">
                    <img src="../../assets/images/contact.jpg" class="w-100 h-100" alt="ảnh công ty">
                    <h1 class="heading--lg">CONTACT</h1>
                </div>
            </div>
        </div>
    </div>

    <div class="grid wide">
        <div class="row">
            <div class="col lg-6 md-7 col-12">
                <div class="side-left">
                    <h2 style="font-size: 1.6rem; color: #409696;">
                        Ivy Academia
                    </h2>

                    <ul class="contact">
                        <li class="contact__item">
                            <font-awesome-icon :icon="['fas', 'map-marker-alt']" class="contact__icon" />
                            <span class="contact__content">
                                Vĩnh Hòa Hưng Nam -  Gò Quao - Kiên Giang
                            </span>
                        </li>
                        <li class="contact__item">
                            <font-awesome-icon :icon="['fas', 'envelope']" class="contact__icon" />
                            <span class="contact__content">
                                phucb2017070@student.ctu.edu.vn
                            </span>
                        </li>
                        <li class="contact__item">
                            <font-awesome-icon :icon="['fas', 'phone']" class="contact__icon" />
                            <span class="contact__content">
                                039 424 1676
                            </span>
                        </li>
                        <li class="contact__item">
                            <font-awesome-icon :icon="['fas', 'home']" class="contact__icon" />
                            <span class="contact__content">
                                www.ivyacademia.edu.com
                            </span>
                        </li>
                        <li class="contact__item">
                            <font-awesome-icon :icon="['fab', 'youtube']" class="contact__icon" />
                            <span class="contact__content">
                                Ivy Academia Offical
                            </span>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="col lg-6 md-5 col-12">
                <div class="side--right" style="text-align: right;">
                    <img src="../../assets/images/contact2.jpg" alt="ảnh">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.grid:not(.wide) {
    margin-top: -20px;
}

.grid.wide {
    margin-top: 2rem;
    margin-bottom: 2rem;
}

.contact__intro-img {
    position: relative;
    height: 40vh;
    max-height: 45vh;

    img {
        object-fit: cover;
    }
}

.heading--lg {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    letter-spacing: 12px;
    color: aliceblue;
}

.contact {
    list-style: none;
    font-size: 1.4rem;
}

.contact__item {
    display: flex;
    align-items: center;
    margin-top: 1rem;

    .contact__icon {
        font-size: 1.7rem;
        flex: 0.5;
    }

    .contact__content {
        flex: 3;
    }
}

.side--right img {
    width: 70%;
}

@media (max-width: 1023px) {
    .contact {
        list-style: none;
        font-size: 1.1rem;
    }

    .contact__icon {
        font-size: 1.3rem;
        flex: 0.5;
    }

    .side--right img {
        width: 100%;
    }
}

@media (max-width: 739px) {
    .side--right {
        margin-top: 1rem;
    }

    .heading--lg {
        font-size: 3rem;
        letter-spacing: 8px;
    }
}
</style>