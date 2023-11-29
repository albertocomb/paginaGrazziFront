<template>
    <div class="div">
        <div class="div-2">
            <!-- Mobile menu button -->
            <div class="mobile-menu-button" @click="toggleMobileMenu">
                <span></span>
                <span></span>
                <span></span>
            </div>

            <!-- Logo Grazzi -->
            <div class="div-3"><router-link to="/">Grazzi</router-link></div>

            <!-- Navigation links -->
            <div class="div-4" :class="{ 'mobile-menu-open': mobileMenuOpen }">
                <div class="div-5">Inicio</div>
                <div class="div-6"><router-link to="/services">Servicios</router-link></div>
                <div class="div-7"><router-link to="/quiensoy">Quien Soy</router-link></div>
                <div class="div-8">Metodología</div>
            </div>
            <div class="div-9">Contacto</div>
        </div>

        <!-- Mobile menu -->
        <div v-if="mobileMenuOpen" class="mobile-menu">
            <div class="div-5">Inicio</div>
            <div class="div-6"><router-link to="/services">Servicios</router-link></div>
            <div class="div-7"><router-link to="/quiensoy">Quien Soy</router-link></div>
            <div class="div-8">Metodología</div>
        </div>

        <div class="div-10">
            <div class="div-11">
                <div class="column">
                    <div class="div-12"></div>
                </div>
                <div class="column-2">
                    <div class="div-13">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sit amet tellus id mi
                        malesuada faucibus. Curabitur gravida auctor blandit. Donec sed augue laoreet, facilisis diam quis,
                        sodales massa. Integer risus purus, scelerisque in erat eget, ornare tincidunt lacus. Morbi et velit
                        venenatis, molestie mauris sit amet, semper neque. Ut finibus ligula dignissim odio finibus, id
                        consequat quam euismod. Donec eleifend felis sed justo ullamcorper, non vulputate purus venenatis.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/* Tus estilos existentes */

.div {
    background-color: #fff;
    display: flex;
    flex-direction: column;
    padding: 21px 58px 50px;
}

@media (max-width: 991px) {
    .div {
        padding: 0 20px;
    }
}

.div-2 {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
}

@media (max-width: 991px) {
    .div-2 {
        max-width: 100%;
        flex-wrap: wrap;
        justify-content: flex-start;
        /* Alinea los elementos a la izquierda */
    }
}

.div-3 {
    background: linear-gradient(92deg, #4c76c8 19.2%, rgba(81, 181, 64, 0) 204.91%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font: 900 36px Inter, sans-serif;
}

.div-4 {
    display: flex;
    align-items: start;
    justify-content: space-between;
    gap: 20px;
    margin: auto 0;
}

@media (max-width: 991px) {
    .div-4 {
        max-width: 100%;
        flex-wrap: wrap;
        justify-content: flex-end;
        /* Alinea los elementos a la derecha */
    }
}

.div-5 {
    color: #000;
    font: 600 18px Inter, sans-serif;
}

.div-6 {
    color: #000;
    font: 600 18px Inter, sans-serif;
}

.div-7 {
    color: #000;
    align-self: stretch;
    font: 600 18px Inter, sans-serif;
}

.div-8 {
    color: #000;
    font: 600 18px Inter, sans-serif;
}

.div-9 {
    color: #fff;
    justify-content: center;
    align-items: start;
    border-radius: 20px;
    background: linear-gradient(249deg, #7e50a3 15.42%, rgba(159, 59, 59, 0) 113.54%);
    align-self: start;
    margin-top: 5px;
    padding: 10px 13px;
    font: 700 18px Inter, sans-serif;
}

.div-10 {
    align-self: center;
    width: 100%;
    max-width: 1245px;
    margin: 192px 0 257px;
}

@media (max-width: 991px) {
    .div-10 {
        max-width: 100%;
        margin: 40px 0;
    }
}

.div-11 {
    gap: 20px;
    display: flex;
}

@media (max-width: 991px) {
    .div-11 {
        flex-direction: column;
        align-items: stretch;
        gap: 0px;
    }
}

.column {
    display: flex;
    flex-direction: column;
    line-height: normal;
    width: 48%;
    margin-left: 0px;
}

@media (max-width: 991px) {
    .column {
        width: 100%;
    }
}

.div-12 {
    background-color: #f9e4ed;
    display: flex;
    width: 504px;
    height: 389px;
    flex-direction: column;
    margin: 0 auto;
}

@media (max-width: 991px) {
    .div-12 {
        max-width: 100%;
        margin-top: 40px;
    }
}

.column-2 {
    display: flex;
    flex-direction: column;
    line-height: normal;
    width: 52%;
    margin-left: 20px;
}

@media (max-width: 991px) {
    .column-2 {
        width: 100%;
    }
}

.div-13 {
    color: #000;
    margin-top: 31px;
    font: 400 24px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-13 {
        max-width: 100%;
        margin-top: 40px;
    }
}

/* Mobile menu styles */

.mobile-menu-button {
    display: none;
    flex-direction: column;
    cursor: pointer;
}

.mobile-menu-button span {
    width: 25px;
    height: 3px;
    background-color: #000;
    margin: 4px 0;
}

.mobile-menu {
    display: none;
    flex-direction: column;
    background-color: #fff;
    padding: 20px;
    position: absolute;
    top: 20px;
    /* Ajusta la posición según tus necesidades */
    right: 20px;
    /* Ajusta la posición según tus necesidades */
}

.mobile-menu-open .mobile-menu {
    display: flex;
}

@media (max-width: 991px) {
    .div-2 {
        flex-direction: row;
        /* Alinea los elementos en la misma fila */
        justify-content: space-between;
        /* Espaciado entre los elementos */
    }

    .mobile-menu-button {
        display: flex;
        align-self: flex-start;
        /* Alinea el botón a la izquierda */
        margin-top: 10px;
    }

    .div-3 {
        order: 1;
        text-align: left;
    }

    .div-4 {
        display: none;
    }

    .div-9 {
        order: 2;
    }

    .mobile-menu {
        display: flex;
    }

    .mobile-menu-open .div-4 {
        display: flex;
    }
}
</style>

<script>
export default {
    data() {
        return {
            mobileMenuOpen: false,
        };
    },
    methods: {
        toggleMobileMenu() {
            this.mobileMenuOpen = !this.mobileMenuOpen;
        },
    },
};
</script>
