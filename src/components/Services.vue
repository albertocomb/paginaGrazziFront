<template>
    <div class="div">
        <div class="div-2">
            <div class="div-3">Grazzi</div>
            <div class="div-4">
                <div class="div-5"><router-link to="/">Inicio</router-link></div>
                <div class="div-6"><router-link to="/services">Servicios</router-link></div>
                <div class="div-7"><router-link to="/quiensoy">Quien Soy</router-link></div>
                <div class="div-8">Metodología</div>
            </div>
            <div class="div-9">Contacto</div>
        </div>
        <div class="div-10">Services</div>
        <div class="div-11">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sit
            amet tellus id mi malesuada faucibus. Curabitur gravida auctor blandit.
            Donec sed augue laoreet, facilisis diam quis, sodales massa. Integer risus
            purus, scelerisque in erat eget, ornare tincidunt lacus. Morbi et velit
            venenatis, molestie mauris sit amet, semper neque. Ut finibus ligula
            dignissim odio finibus, id consequat quam euismod. Donec eleifend felis
            sed justo ullamcorper, non vulputate purus venenatis.
        </div>
        <div class="div-12"></div>
    </div>
</template>



<style scoped>
.div {
    background-color: #fff;
    display: flex;
    flex-direction: column;
    padding: 21px 57px 50px 50px;
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
        justify-content: center;
    }
}

.div-3 {
    background: linear-gradient(92deg,
            #4c76c8 19.2%,
            rgba(81, 181, 64, 0) 204.91%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    align-self: start;
    flex-grow: 1;
    white-space: nowrap;
    font: 900 36px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-3 {
        white-space: initial;
    }
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
        justify-content: center;
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
    align-self: stretch;
    white-space: nowrap;
    font: 600 18px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-8 {
        white-space: initial;
    }
}

.div-9 {
    color: #fff;
    white-space: nowrap;
    justify-content: center;
    border-radius: 20px;
    background: linear-gradient(249deg,
            #7e50a3 15.42%,
            rgba(159, 59, 59, 0) 113.54%);
    align-self: start;
    margin-top: 5px;
    padding: 10px 14px;
    font: 700 18px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-9 {
        white-space: initial;
    }
}

.div-10 {
    color: #000;
    align-self: center;
    margin-top: 128px;
    white-space: nowrap;
    font: 600 48px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-10 {
        font-size: 40px;
        margin-top: 40px;
        white-space: initial;
    }
}

.div-11 {
    color: #000;
    margin-top: 35px;
    font: 400 24px Inter, sans-serif;
}

@media (max-width: 991px) {
    .div-11 {
        max-width: 100%;
    }
}

.div-12 {
    background-color: #d9d9d9;
    align-self: center;
    display: flex;
    width: 515px;
    height: 359px;
    flex-direction: column;
    margin: 37px 0 133px;
}

@media (max-width: 991px) {
    .div-12 {
        max-width: 100%;
        margin-bottom: 40px;
    }
}
</style>