<template>
    <div class="div">
        <div class="div-2">
            <!-- Mobile menu button -->
            <div class="mobile-menu-button" @click="toggleMobileMenu">
                <span></span>
                <span></span>
                <span></span>
            </div>

            <!-- Logo -->
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
                        <!-- Tu contenido aquí -->
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>


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
}

.mobile-menu-open .mobile-menu {
    display: flex;
}

@media (max-width: 991px) {
    .div-2 {
        flex-direction: column;
        align-items: stretch;
    }

    .mobile-menu-button {
        display: flex;
        align-self: flex-end;
        /* Alinea el botón a la derecha */
        margin-top: 10px;
        /* Espaciado superior */
    }

    .div-3 {
        order: 1;
        text-align: left;
        /* Alinea el logo a la izquierda */
    }

    .div-4 {
        display: none;
    }

    .div-9 {
        order: 2;
    }

    .mobile-menu {
        display: flex;
        position: absolute;
        /* Asegura que el menú desplegable está fuera del flujo normal del documento */
        top: 60px;
        /* Ajusta la posición vertical del menú desplegable */
        right: 20px;
        /* Ajusta la posición horizontal del menú desplegable */
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
