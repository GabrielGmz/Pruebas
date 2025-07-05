<template>
    <div class="content">
        <!-- Dedicatoria principal -->
        <div class="dedication">
            <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
                <linearGradient id="8UoUdlQgDhwTWW8a0N~~fa_AJsZdj4SRgq1_gr1" x1="18.495" x2="18.017" y1="16.149"
                    y2="41.218" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#7b83eb"></stop>
                    <stop offset="1" stop-color="#5961c3"></stop>
                </linearGradient>
                <polygon fill="url(#8UoUdlQgDhwTWW8a0N~~fa_AJsZdj4SRgq1_gr1)"
                    points="23,30.591 14,33.864 14,1.136 23,8.5"></polygon>
                <linearGradient id="8UoUdlQgDhwTWW8a0N~~fb_AJsZdj4SRgq1_gr2" x1="29.592" x2="29.114" y1="16.36"
                    y2="41.429" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#7b83eb"></stop>
                    <stop offset="1" stop-color="#5961c3"></stop>
                </linearGradient>
                <polygon fill="url(#8UoUdlQgDhwTWW8a0N~~fb_AJsZdj4SRgq1_gr2)"
                    points="25,30.591 34,33.864 34,1.136 25,8.5"></polygon>
                <linearGradient id="8UoUdlQgDhwTWW8a0N~~fc_AJsZdj4SRgq1_gr3" x1="24.376" x2="23.898" y1="16.261"
                    y2="41.33" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#7b83eb"></stop>
                    <stop offset="1" stop-color="#5961c3"></stop>
                </linearGradient>
                <polygon fill="url(#8UoUdlQgDhwTWW8a0N~~fc_AJsZdj4SRgq1_gr3)"
                    points="21.824,38 23,38 23,46 25,46 25,38 26.176,38 27,36 21,36"></polygon>
                <linearGradient id="8UoUdlQgDhwTWW8a0N~~fd_AJsZdj4SRgq1_gr4" x1="16.955" x2="16.477" y1="16.12"
                    y2="41.188" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#7b83eb"></stop>
                    <stop offset="1" stop-color="#5961c3"></stop>
                </linearGradient>
                <path fill="url(#8UoUdlQgDhwTWW8a0N~~fd_AJsZdj4SRgq1_gr4)"
                    d="M17,36h-3v10h3c1.103,0,2-0.897,2-2v-2c0-0.366-0.106-0.705-0.278-1 C18.894,40.705,19,40.366,19,40v-2C19,36.897,18.103,36,17,36z M16,38h1l0.001,2H17h-1V38z M16,44v-2h1l0.001,2H16z">
                </path>
                <linearGradient id="8UoUdlQgDhwTWW8a0N~~fe_AJsZdj4SRgq1_gr5" x1="31.968" x2="31.491" y1="16.406"
                    y2="41.474" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#7b83eb"></stop>
                    <stop offset="1" stop-color="#5961c3"></stop>
                </linearGradient>
                <path fill="url(#8UoUdlQgDhwTWW8a0N~~fe_AJsZdj4SRgq1_gr5)"
                    d="M34,39v-1c0-1.103-0.897-2-2-2h-1c-1.103,0-2,0.897-2,2v1.465 c0,0.67,0.333,1.292,0.891,1.664L32,42.535V44h-1v-1h-2v1c0,1.103,0.897,2,2,2h1c1.103,0,2-0.897,2-2v-1.465 c0-0.67-0.333-1.292-0.891-1.664L31,39.465V38h1v1H34z">
                </path>
            </svg>
            <h1>Para mi chica especial 💜</h1>
            <p>
                Como diría BTS, <strong>"You never walk alone"</strong>. Gracias por iluminar mi mundo con tu
                sonrisa y
                tu cariño.
                Esta dedicatoria es solo para ti, con todo mi amor y un toque de magia morada.
            </p>
            <button class="modal-btn" @click="showModal = true">
                Abrir Detalles 💜
            </button>
        </div>

        <!-- Modal personalizado -->
        <transition name="modal-fade">
            <div class="modal-overlay" v-if="showModal" @click.self="showModal = false">
                <div class="modal-content">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Jimin_on_the_way_to_SBS_Radio%2C_31_March_2023_%282%29.jpg"
                        alt="BTS Heart" class="bts-heart" />
                    <h2>Te quiero hasta el infinito y más allá 💜</h2>
                    <p>
                        Eres mi bias, mi melodía favorita y la razón por la que cada día es especial.
                        Como en las canciones de BTS, contigo todo es posible.
                        <br><br>
                        <em>"Cause I, I, I'm in the stars tonight..."</em>
                    </p>
                    <button class="close-btn" @click="showModal = false">Cerrar</button>
                </div>
            </div>
        </transition>

        <!-- Animación sutil de corazones -->
        <div class="hearts-animation">
            <span v-for="n in 7" :key="n" class="heart"
                :style="{ left: `${n * 12}%`, animationDelay: `${n * 0.5}s` }">💜</span>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue'
const showModal = ref(false)
</script>

<style scoped>
.content {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: 'Poppins', 'Segoe UI', Arial, sans-serif;
    background: linear-gradient(135deg, #f8e1ff 0%, #e3f0ff 100%);
    min-height: 100vh;
    padding: 2.5rem 1.2rem;
    position: relative;
    overflow-x: hidden;
}

.dedication {
    background: rgba(255, 255, 255, 0.92);
    border-radius: 2rem;
    box-shadow: 0 8px 32px rgba(136, 58, 255, 0.13), 0 1.5px 8px #b983ff33;
    padding: 2.5rem 1.5rem;
    text-align: center;
    max-width: 420px;
    margin: 0 auto;
    border: 2px solid #e3c0ff;
    position: relative;
    z-index: 2;
}

.bts-logo {
    width: 70px;
    margin-bottom: 1.2rem;
    filter: drop-shadow(0 2px 12px #b983ff77);
    transition: transform 0.3s;
}

.bts-logo:hover {
    transform: scale(1.08) rotate(-8deg);
}

.dedication h1 {
    color: #a259ff;
    font-size: 2.2rem;
    margin-bottom: 0.7rem;
    font-weight: 800;
    letter-spacing: 1px;
    text-shadow: 0 2px 8px #f8e1ff88;
}

.dedication p {
    color: #5a189a;
    font-size: 1.15rem;
    margin-bottom: 1.7rem;
    line-height: 1.6;
    background: linear-gradient(90deg, #b983ff22 0%, #f8e1ff33 100%);
    border-radius: 1rem;
    padding: 0.7rem 0.5rem;
}

.modal-btn {
    background: linear-gradient(90deg, #b983ff 0%, #f8e1ff 100%);
    color: #fff;
    border: none;
    border-radius: 2rem;
    padding: 0.9rem 2.2rem;
    font-size: 1.08rem;
    font-weight: 700;
    cursor: pointer;
    transition: background 0.3s, transform 0.2s;
    box-shadow: 0 2px 12px #b983ff33;
    letter-spacing: 0.5px;
}

.modal-btn:hover {
    background: linear-gradient(90deg, #a259ff 0%, #b983ff 100%);
    transform: scale(1.04);
}

.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(185, 131, 255, 0.18);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1000;
    backdrop-filter: blur(2.5px);
}

.modal-content {
    background: #fff;
    border-radius: 1.5rem;
    padding: 2.2rem 1.4rem;
    max-width: 350px;
    text-align: center;
    box-shadow: 0 12px 40px #b983ff55, 0 2px 12px #e3c0ff33;
    animation: pop-in 0.45s cubic-bezier(.68, -0.55, .27, 1.55);
    border: 2px solid #e3c0ff;
    position: relative;
}

@keyframes pop-in {
    0% {
        transform: scale(0.8) translateY(40px);
        opacity: 0;
    }

    100% {
        transform: scale(1) translateY(0);
        opacity: 1;
    }
}

.bts-heart {
    width: 54px;
    margin-bottom: 1.1rem;
    filter: drop-shadow(0 2px 12px #b983ff77);
    animation: beat 1.2s infinite;
}

@keyframes beat {

    0%,
    100% {
        transform: scale(1);
    }

    20% {
        transform: scale(1.15);
    }

    40% {
        transform: scale(0.95);
    }

    60% {
        transform: scale(1.1);
    }

    80% {
        transform: scale(0.98);
    }
}

.modal-content h2 {
    color: #a259ff;
    font-size: 1.45rem;
    margin-bottom: 0.8rem;
    font-weight: 800;
    letter-spacing: 0.5px;
    text-shadow: 0 2px 8px #f8e1ff66;
}

.modal-content p {
    color: #5a189a;
    font-size: 1.08rem;
    margin-bottom: 1.6rem;
    line-height: 1.6;
    background: linear-gradient(90deg, #b983ff22 0%, #f8e1ff33 100%);
    border-radius: 0.8rem;
    padding: 0.7rem 0.5rem;
}

.close-btn {
    background: #b983ff;
    color: #fff;
    border: none;
    border-radius: 1.5rem;
    padding: 0.7rem 1.7rem;
    font-size: 1.05rem;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
    box-shadow: 0 2px 8px #b983ff33;
}

.close-btn:hover {
    background: #a259ff;
    transform: scale(1.05);
}

.modal-fade-enter-active,
.modal-fade-leave-active {
    transition: opacity 0.3s;
}

.modal-fade-enter-from,
.modal-fade-leave-to {
    opacity: 0;
}

.hearts-animation {
    position: fixed;
    bottom: 10px;
    left: 0;
    right: 0;
    pointer-events: none;
    z-index: 10;
    height: 80px;
}

.heart {
    position: absolute;
    font-size: 2.1rem;
    animation: floatUp 3.2s infinite;
    opacity: 0.8;
    filter: drop-shadow(0 2px 8px #b983ff77);
    transition: filter 0.2s;
}

.heart:hover {
    filter: drop-shadow(0 4px 16px #a259ffcc);
}

@keyframes floatUp {
    0% {
        bottom: 0;
        opacity: 0.8;
        transform: translateY(0) scale(1);
    }

    60% {
        opacity: 1;
        transform: translateY(-30px) scale(1.1);
    }

    100% {
        bottom: 80px;
        opacity: 0;
        transform: translateY(-80px) scale(0.95);
    }
}

@media (max-width: 480px) {

    .dedication,
    .modal-content {
        padding: 1.2rem 0.7rem;
        max-width: 97vw;
    }

    .bts-logo,
    .bts-heart {
        width: 38px;
    }

    .dedication h1 {
        font-size: 1.25rem;
    }

    .modal-content h2 {
        font-size: 1.05rem;
    }

    .heart {
        font-size: 1.3rem;
    }
}
</style>
