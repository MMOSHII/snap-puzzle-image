<template>
    <div class="app-root font-body text-ink overflow-x-hidden min-h-screen bg-[#fdfbf7]">
        <div v-if="appState === 'landing'" class="fixed inset-0 z-[200] bg-[#fdfbf7] overflow-y-auto overflow-x-hidden flex flex-col">
            <header class="fixed top-4 left-0 w-full z-[210] px-4">
                <div class="flex justify-between items-center w-full max-w-[1200px] mx-auto px-6 py-3 bg-white cutout-shadow rounded-2xl rotate-1">
                    <a class="flex items-center gap-2 font-marker text-3xl font-bold transition-transform hover:scale-105" href="#">
                        <span class="material-symbols-outlined text-rose-400">favorite</span>
                        Puzzle Cam
                    </a>
                    <nav class="hidden md:flex gap-6 font-handwriting text-2xl font-bold text-stone-600">
                        <a class="hover:text-rose-500 hover:-translate-y-1 transition-all" href="#">Home</a>
                        <a class="hover:text-amber-500 hover:-translate-y-1 transition-all" href="#how-it-works">How it works</a>
                        <a class="hover:text-sky-500 hover:-translate-y-1 transition-all" href="#features">Goodies</a>
                        <a class="hover:text-emerald-500 hover:-translate-y-1 transition-all" href="#archive">My Scrapbook</a>
                    </nav>
                </div>
            </header>

            <main class="flex-grow pt-24 pb-20">
                <section class="relative min-h-[90vh] flex flex-col items-center justify-center text-center px-4">
                    <div class="absolute top-10 left-10 w-24 h-8 washi-tape washi-pink -rotate-12 z-20"></div>
                    <div class="absolute bottom-20 right-10 w-32 h-8 washi-tape washi-yellow rotate-6 z-20"></div>

                    <div class="relative z-10 bg-white p-10 md:p-20 cutout-shadow rounded-3xl max-w-4xl mx-auto -rotate-1 hover:rotate-0 transition-transform">
                        <div class="absolute -top-4 left-1/2 -translate-x-1/2 w-40 h-8 washi-tape washi-blue z-20 rotate-2"></div>
                        <h1 class="font-marker text-6xl md:text-8xl font-bold text-ink mb-6">Make Cute Memories!</h1>
                        <p class="font-handwriting text-3xl text-stone-600 mb-10 max-w-2xl mx-auto">
                            Use simple hand gestures to snap fun photos, solve them like a puzzle, and build your very own digital scrapbook. 📸✨
                        </p>
                        <button @click="appState = 'welcome'" class="bg-rose-300 px-10 py-4 cutout-shadow rounded-full font-marker text-4xl font-bold hover:bg-rose-400 hover:-translate-y-2 active:translate-y-1 transition-all">
                            Let's Start!
                        </button>
                    </div>
                </section>
                <section class="py-20 px-4 relative" id="how-it-works">
                    <h2 class="font-marker text-6xl font-bold text-center mb-16 underline decoration-wavy decoration-sky-300">
                        How to Play!
                    </h2>

                    <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-10">
                        <div class="polaroid rotate-3 hover:rotate-0 transition-all group">
                            <div class="absolute -top-3 left-4 w-16 h-6 washi-tape washi-pink -rotate-6 z-10"></div>
                            <div class="w-full h-48 bg-rose-100 flex items-center justify-center mb-4 border border-rose-200">
                                <span class="material-symbols-outlined text-6xl text-rose-400 group-hover:scale-125 transition-transform">
                                    pinch
                                </span>
                            </div>
                            <h3 class="font-marker text-4xl font-bold text-center mb-2">
                                1. Snap!
                            </h3>
                            <p class="font-handwriting text-2xl text-center text-stone-600">
                                Pinch your fingers to take a photo!
                            </p>
                        </div>

                        <div class="polaroid -rotate-2 hover:rotate-0 transition-all group mt-0 md:mt-10">
                            <div class="absolute -top-3 right-4 w-20 h-6 washi-tape washi-yellow rotate-6 z-10"></div>
                            <div class="w-full h-48 bg-amber-100 flex items-center justify-center mb-4 border border-amber-200">
                                <span class="material-symbols-outlined text-6xl text-amber-400 group-hover:scale-125 transition-transform">
                                    drag_pan
                                </span>
                            </div>
                            <h3 class="font-marker text-4xl font-bold text-center mb-2">
                                2. Solve!
                            </h3>
                            <p class="font-handwriting text-2xl text-center text-stone-600">
                                The photo shatters! Drag pieces to fix it.
                            </p>
                        </div>
                        <div class="polaroid rotate-2 hover:rotate-0 transition-all group">
                            <div class="absolute -top-3 left-1/2 -translate-x-1/2 w-16 h-6 washi-tape washi-blue -rotate-2 z-10"></div>
                            <div class="w-full h-48 bg-sky-100 flex items-center justify-center mb-4 border border-sky-200">
                                <span class="material-symbols-outlined text-6xl text-sky-400 group-hover:scale-125 transition-transform">
                                    front_hand
                                </span>
                            </div>
                            <h3 class="font-marker text-4xl font-bold text-center mb-2">
                                3. Save!
                            </h3>
                            <p class="font-handwriting text-2xl text-center text-stone-600">
                                Make a fist to save it to your scrapbook!
                            </p>
                        </div>
                    </div>
                </section>
                <section class="py-20 px-4 relative" id="features">
                    <h2 class="font-marker text-6xl font-bold text-center mb-16 underline decoration-wavy decoration-emerald-300">Scrapbook Goodies</h2>
                    <div class="max-w-6xl mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8">
                        <div class="polaroid rotate-2">
                            <span class="material-symbols-outlined text-emerald-400 text-5xl mb-4">blur_on</span>
                            <h4 class="font-marker text-3xl font-bold mb-2">Cute Filters</h4>
                            <p class="font-handwriting text-xl text-stone-600">Vintage, B&W, and more cute effects for your photos!</p>
                        </div>
                        <div class="polaroid -rotate-3">
                            <span class="material-symbols-outlined text-rose-400 text-5xl mb-4">grid_view</span>
                            <h4 class="font-marker text-3xl font-bold mb-2">Photo Grids</h4>
                            <p class="font-handwriting text-xl text-stone-600">Choose between 3x3 or 4x4 grids to solve your puzzle.</p>
                        </div>
                        <div class="polaroid rotate-1">
                            <span class="material-symbols-outlined text-amber-400 text-5xl mb-4">animation</span>
                            <h4 class="font-marker text-3xl font-bold mb-2">Stickers!</h4>
                            <p class="font-handwriting text-xl text-stone-600">Decorate your finished photos with cute emojis and frames.</p>
                        </div>
                        <div class="polaroid -rotate-2">
                            <span class="material-symbols-outlined text-sky-400 text-5xl mb-4">speed</span>
                            <h4 class="font-marker text-3xl font-bold mb-2">Super Fast</h4>
                            <p class="font-handwriting text-xl text-stone-600">Works right in your browser, no apps needed!</p>
                        </div>
                    </div>
                </section>
                <section class="py-20 px-4 relative bg-stone-100" id="archive">
                    <div class="absolute top-0 left-0 w-full h-4 bg-[url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMCIgaGVpZ2h0PSIxMCI+PHBhdGggZD0iTTAgMGw1IDEwTDEwIDBWMEgwemoiIGZpbGw9IiNmZGZiZjciLz48L3N2Zz4=')]"></div>
                        <h2 class="font-marker text-6xl font-bold text-center mb-16 underline decoration-wavy decoration-rose-300 mt-10">My Scrapbook</h2>
                        <div class="max-w-5xl mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10" id="galleryContainer">
                        <div class="polaroid rotate-3 hover:scale-105 transition-transform">
                            <div class="w-full h-64 bg-stone-200 mb-4 overflow-hidden flex items-center justify-center">
                                <span class="font-handwriting text-3xl text-stone-400">Empty Page!</span>
                            </div>
                            <div class="font-marker text-2xl font-bold text-center">Take a photo to start!</div>
                        </div>
                    </div>
                </section>
            </main>
        </div>

        <!-- ================= WELCOME / SETTINGS SCREEN ================= -->
        <div v-if="appState === 'welcome'" class="fixed inset-0 z-[200] flex flex-col items-center justify-center bg-[#fdfbf7] p-4">
            <div class="bg-white p-10 cutout-shadow rounded-3xl max-w-4xl w-full relative -rotate-1">
                <div class="absolute -top-4 left-1/2 -translate-x-1/2 w-48 h-10 washi-tape washi-pink z-20 rotate-3"></div>
                <h2 class="font-marker text-6xl font-bold text-center mb-8">Setup Your Scrapbook! 🎨</h2>
                <div class="mb-10">
                    <h3 class="font-handwriting text-3xl font-bold text-stone-600 mb-4">Choose Puzzle Size:</h3>
                    <div class="flex flex-wrap gap-4 justify-center">
                        <button v-for="size in [2, 3, 4]" :key="`grid-${size}`" @click="config.grid = size"
                                :class="['cutout-shadow px-8 py-4 rounded-xl font-marker text-4xl transition-transform relative hover:-translate-y-1', 
                                        config.grid === size ? 'bg-amber-100 rotate-2' : 'bg-white -rotate-1']">
                            {{ size }}x{{ size }} Grid
                            <span :class="['absolute -top-3 -right-3 text-rose-500 material-symbols-outlined text-4xl transition-opacity', config.grid === size ? 'opacity-100' : 'opacity-0']">favorite</span>
                        </button>
                    </div>
                </div>
                <div class="mb-10">
                    <h3 class="font-handwriting text-3xl font-bold text-stone-600 mb-4">How many photos?</h3>
                    <div class="flex flex-wrap gap-4 justify-center">
                        <button v-for="layout in [2, 3, 4]" :key="`layout-${layout}`" @click="config.layout = layout"
                                :class="['cutout-shadow px-8 py-4 rounded-xl font-marker text-4xl transition-transform relative hover:-translate-y-1', 
                                        config.layout === layout ? 'bg-sky-100 -rotate-1' : 'bg-white rotate-1']">
                            {{ layout }} Photos
                            <span :class="['absolute -top-3 -right-3 text-rose-500 material-symbols-outlined text-4xl transition-opacity', config.layout === layout ? 'opacity-100' : 'opacity-0']">favorite</span>
                        </button>
                    </div>
                </div>
                <div class="mb-10">
                    <h3 class="font-handwriting text-3xl font-bold text-stone-600 mb-4">Pick a Filter!</h3>
                    <div class="flex flex-wrap gap-4 justify-center">
                        <button v-for="filter in [{id: 'none', label: 'Normal'}, {id: 'bw', label: 'B&W'}, {id: 'vintage', label: 'Vintage'}]" :key="filter.id" 
                                @click="config.filter = filter.id"
                                :class="['cutout-shadow px-6 py-2 rounded-full font-handwriting text-2xl font-bold transition-all', 
                                        config.filter === filter.id ? 'bg-emerald-200 scale-110' : 'bg-white hover:scale-105']">
                            {{ filter.label }}
                        </button>
                    </div>
                </div>

                <div class="text-center">
                    <button @click="appState = 'tutorial'" class="bg-rose-300 px-12 py-4 cutout-shadow rounded-full font-marker text-5xl font-bold hover:bg-rose-400 hover:-translate-y-2 transition-all">
                        Open Camera! 📸
                    </button>
                </div>
            </div>
        </div>

        <!-- ================= TUTORIAL SCREEN ================= -->
        <div v-if="appState === 'tutorial'" class="fixed inset-0 z-[200] flex flex-col items-center justify-center bg-black/50 backdrop-blur-sm p-4">
            <div class="bg-white p-10 cutout-shadow rounded-3xl max-w-2xl w-full relative rotate-1">
                <div class="absolute -top-4 left-1/2 -translate-x-1/2 w-32 h-10 washi-tape washi-yellow z-20 -rotate-2"></div>
                <h2 class="font-marker text-6xl font-bold text-center mb-6">Quick Guide!</h2>
                <ul class="font-handwriting text-3xl space-y-4 mb-8">
                    <li class="flex items-center gap-4"><span class="material-symbols-outlined text-4xl text-rose-400">pinch</span> Pinch to take a photo</li>
                    <li class="flex items-center gap-4"><span class="material-symbols-outlined text-4xl text-amber-400">drag_pan</span> Drag to solve the puzzle</li>
                    <li class="flex items-center gap-4"><span class="material-symbols-outlined text-4xl text-sky-400">front_hand</span> Clench fist to save it!</li>
                </ul>
                <div class="text-center">
                    <button @click="startApp" class="bg-emerald-300 px-8 py-3 cutout-shadow rounded-full font-marker text-4xl font-bold hover:bg-emerald-400 transition-all">
                        Got it! 👍
                    </button>
                </div>
            </div>
        </div>

        <!-- ================= MAIN APP / CAMERA SCREEN ================= -->
        <div v-show="['tracking', 'countdown', 'puzzle', 'shattering'].includes(appState)" class="relative w-full h-screen bg-paper flex-col overflow-hidden items-center justify-center p-4">
            <div class="relative w-full max-w-4xl aspect-[4/3] bg-white cutout-shadow p-4 pb-16 rotate-1 polaroid-container">
                <div class="absolute top-0 left-1/2 -translate-x-1/2 w-48 h-8 washi-tape washi-blue -rotate-1 z-20"></div>
                
                <div class="relative w-full h-full overflow-hidden stitched-border bg-stone-100 rounded-lg">
                    <video ref="videoEl" autoplay playsinline class="hidden"></video>
                    <canvas ref="sceneCanvas" class="w-full h-full object-cover transform scale-x-[-1]"></canvas>

                    <div v-if="isLoading" class="absolute inset-0 bg-white/80 flex flex-col items-center justify-center z-50">
                        <span class="material-symbols-outlined text-6xl text-rose-400 animate-spin mb-4">refresh</span>
                        <p class="font-handwriting text-3xl font-bold">{{ loaderText }}</p>
                    </div>
                </div>
                <p class="font-marker text-4xl text-center mt-4 text-stone-600">Making memories...</p>
            </div>

            <div class="absolute top-6 left-6 bg-white cutout-shadow px-6 py-2 rounded-full flex items-center gap-3 -rotate-2">
                <div :class="['w-4 h-4 rounded-full animate-pulse', statusDotClass]"></div>
                <span class="font-handwriting text-2xl font-bold">{{ statusText }}</span>
            </div>

            <div class="absolute top-6 right-6 flex items-center gap-4">
                <div class="bg-white cutout-shadow px-6 py-2 rounded-full font-handwriting text-2xl font-bold rotate-2">
                    <span>{{ galleryEntries.length }} / {{ config.layout }}</span>
                </div>
            </div>
        </div>

        <!-- ================= PRINTING SCREEN ================= -->
        <div v-if="appState === 'printing'" class="fixed inset-0 z-50 flex flex-col items-center justify-center bg-sky-100">
            <h2 class="font-marker text-6xl md:text-8xl font-bold text-ink mb-12 text-center underline decoration-wavy decoration-rose-300">Printing...</h2>
            <div class="relative flex flex-col items-center w-full max-w-sm">
                <div class="w-64 md:w-80 h-10 bg-white rounded-xl cutout-shadow border-4 border-ink flex items-center justify-center relative z-20">
                    <div class="w-48 md:w-64 h-3 bg-stone-800 rounded-full shadow-inner"></div>
                </div>
                <div class="relative w-40 md:w-48 h-[280px] md:h-[380px] overflow-hidden -mt-4 z-10" style="perspective: 1000px;">
                    <img :src="printingImageSrc" class="w-full absolute top-0 left-0 shadow-lg border-[8px] border-white bg-white transition-transform duration-[3000ms] ease-out" :class="isPrintingAnimated ? 'translate-y-0' : '-translate-y-[120%]'">
                </div>
            </div>
        </div>

        <!-- ================= EDITING SCREEN ================= -->
        <div v-show="appState === 'edit_photo'" class="fixed inset-0 z-50 bg-[#fdfbf7] flex-col md:flex-row p-4 overflow-hidden" :class="appState === 'edit_photo' ? 'flex' : 'hidden'">
            <div class="flex-grow flex items-center justify-center relative p-4 sm:p-8 min-h-0">
                <div class="absolute top-10 left-10 w-32 sm:w-48 h-10 washi-tape washi-yellow -rotate-6 z-10"></div>
                <div class="absolute bottom-10 right-10 w-32 sm:w-48 h-10 washi-tape washi-blue rotate-6 z-10"></div>
                
                <div class="relative cutout-shadow bg-white p-3 sm:p-5 flex-shrink-0">
                    <canvas ref="editCanvas" @mousedown="handleDragStart" @touchstart.passive="false" style="max-width: 100%; max-height: calc(100vh - 6rem); object-fit: contain;"></canvas>
                </div>
            </div>

            <aside class="w-full md:w-96 bg-white cutout-shadow rounded-3xl p-6 overflow-y-auto flex flex-col gap-8 -rotate-1 h-full max-h-[95vh] self-center">
                <h2 class="font-marker text-6xl text-center underline decoration-wavy decoration-rose-300">Decorate!</h2>

                <div>
                    <h3 class="font-handwriting text-3xl mb-4 font-bold">Pick a Frame</h3>
                    <div class="flex flex-wrap gap-3">
                        <button v-for="color in ['#292524', '#fb7185', '#38bdf8', '#34d399', '#ffffff']" :key="color"
                                @click="setBorderColor(color)"
                                :class="['bg-white cutout-shadow w-12 h-12 rounded-full border-4', 
                                        currentBorderColor === color ? 'scale-125 ring-4 ring-stone-400 ring-offset-2' : '']"
                                :style="{ borderColor: color }">
                        </button>
                    </div>
                </div>

                <div>
                    <h3 class="font-handwriting text-3xl mb-4 font-bold">Cute Stickers</h3>
                    <div class="flex flex-wrap gap-3">
                        <button v-for="emoji in ['✨', '💖', '🌸', '⭐', '🎀', '☁️']" :key="emoji"
                                @click="addSticker(emoji)"
                                class="sticker-btn bg-amber-50 cutout-shadow p-2 text-3xl rounded-xl hover:-translate-y-1 transition-transform">
                            {{ emoji }}
                        </button>
                    </div>
                    <p class="font-handwriting text-xl text-stone-500 mt-2">Click to add, drag to move!</p>
                </div>

                <div ref="trashBin" :class="['w-full h-24 border-4 border-dashed rounded-2xl flex flex-col items-center justify-center transition-colors', 
                                            isHoveringTrash ? 'bg-rose-400 text-white border-rose-500 scale-110 opacity-100' : 'border-rose-300 text-rose-400 bg-rose-50 opacity-70 scale-105']">
                    <span class="material-symbols-outlined text-4xl">delete</span>
                    <span class="font-handwriting text-2xl font-bold">Trash</span>
                </div>

                <div class="mt-auto flex flex-col gap-3">
                    <button @click="finishEditAndReturn(true)" class="w-full bg-emerald-300 hover:bg-emerald-400 cutout-shadow py-4 rounded-xl font-marker text-4xl font-bold transition-transform active:translate-y-1">
                        Save Scrapbook!
                    </button>
                    <button @click="finishEditAndReturn(false)" class="w-full bg-stone-200 hover:bg-stone-300 cutout-shadow py-3 rounded-xl font-marker text-3xl font-bold transition-transform active:translate-y-1">
                        Skip
                    </button>
                </div>
            </aside>
        </div>
    </div>
</template>

<script setup>
import {
    ref,
    reactive,
    onMounted,
    onUnmounted
} from 'vue';
import {
    FilesetResolver,
    HandLandmarker
} from "https://cdn.jsdelivr.net/npm/@mediapipe/tasks-vision@0.10.14";

// ==========================================
// 1. STATE & REFS
// ==========================================

// Template Refs
const videoEl = ref(null);
const sceneCanvas = ref(null);
const editCanvas = ref(null);
const trashBin = ref(null);

// UI State
const appState = ref('landing');
const isLoading = ref(false);
const loaderText = ref('');
const statusText = ref('Ready!');
const statusDotClass = ref('bg-emerald-400');
const galleryEntries = ref([]);

// Configuration State
const config = reactive({
    grid: 3,
    layout: 3,
    filter: 'none'
});

// Printing State
const printingImageSrc = ref('');
const isPrintingAnimated = ref(false);

// Editor State
const currentBorderColor = ref('#ffffff');
const isHoveringTrash = ref(false);
let placedStickers = [];
let currentEditCanvas = null;
let draggingStickerIndex = -1;
let dragOffsetX = 0;
let dragOffsetY = 0;

// Game & MediaPipe State
const puzzle = reactive({
    boardBox: null,
    pieces: [],
    solved: false,
    tileW: 0,
    tileH: 0,
    fullPhotoboothCanvas: null
});

const drag = reactive({
    activeHand: null,
    piece: null,
    offsetX: 0,
    offsetY: 0,
});

const countdown = reactive({
    active: false,
    startedAt: 0,
});

const shatter = reactive({
    active: false,
    startedAt: 0,
    fragments: [],
    pendingCanvas: null,
});

const freezeGate = {
    holding: false,
    since: 0
};
const lastSeenFrame = {
    box: null,
    at: 0
};
let fistHoldCounter = 0;
let handLandmarker = null;
let visionInstance = null;
let loopRunning = false;
let lastDetectTime = 0;
let currentLandmarks = [];
let currentHandedness = [];
let isFallbackActive = false;

// ==========================================
// 2. CONSTANTS
// ==========================================

const LM = {
    WRIST: 0,
    THUMB_TIP: 4,
    INDEX_MCP: 5,
    INDEX_TIP: 8,
    MIDDLE_TIP: 12,
    RING_TIP: 16,
    PINKY_TIP: 20,
    MIDDLE_MCP: 9,
    RING_MCP: 13,
    PINKY_MCP: 17
};
const PINCH_THRESHOLD = 0.055;
const FRAME_PADDING = 28;
const FREEZE_HOLD_MS = 250;
const COUNTDOWN_SECONDS = 3;
const FIST_HOLD_FRAMES = 12;
const SNAP_DISTANCE_RATIO = 0.45;
const LOAD_TIMEOUT_MS = 60000;
const SHATTER_DURATION_MS = 850;
const FRAME_GRACE_MS = 450;
const DISPLACE_ANIM_MS = 220;

const PHOTOBOOTH_CONTRAST_ALPHA = 1.3;
const PHOTOBOOTH_BRIGHTNESS_BETA = 10;
const PHOTOBOOTH_NOISE_STD = 15;

const HAND_CONNECTIONS = [
    [0, 1],
    [1, 2],
    [2, 3],
    [3, 4],
    [0, 5],
    [5, 6],
    [6, 7],
    [7, 8],
    [5, 9],
    [9, 10],
    [10, 11],
    [11, 12],
    [9, 13],
    [13, 14],
    [14, 15],
    [15, 16],
    [13, 17],
    [17, 18],
    [18, 19],
    [19, 20],
    [0, 17],
];


// ==========================================
// 3. INITIALIZATION & CAMERA
// ==========================================

const startApp = async () => {
    appState.value = 'tracking';
    isLoading.value = true;
    loaderText.value = "requesting camera access…";

    try {
        if (!videoEl.value.srcObject) {
            await initWebcam();
        }

        if (!handLandmarker) {
            loaderText.value = "loading HandLandmarker model…";
            handLandmarker = await initHandLandmarker();
        }

        isLoading.value = false;
        statusDotClass.value = "bg-emerald-400";
        statusText.value = "ready";

        if (!loopRunning) {
            loopRunning = true;
            requestAnimationFrame(renderLoop);
        }
    } catch (err) {
        isLoading.value = false;
        console.error(err);
        statusText.value = "Camera or Model Error";
        statusDotClass.value = "bg-rose-500";
    }
};

async function initWebcam() {
    if (!navigator.mediaDevices?.getUserMedia) throw new Error("This browser does not support camera access.");
    const isMobile = /Mobi|Android|iPhone|iPad/i.test(navigator.userAgent);
    const stream = await navigator.mediaDevices.getUserMedia({
        video: {
            width: {
                ideal: isMobile ? 1280 : 1920
            },
            height: {
                ideal: isMobile ? 720 : 1080
            },
            facingMode: "user"
        },
        audio: false,
    });

    videoEl.value.srcObject = stream;
    await new Promise((resolve) => {
        videoEl.value.onloadedmetadata = () => {
            videoEl.value.play();
            resolve();
        };
    });

    sceneCanvas.value.width = videoEl.value.videoWidth;
    sceneCanvas.value.height = videoEl.value.videoHeight;
}

function withTimeout(promise, ms, timeoutMessage) {
    let timer;
    const timeout = new Promise((_, reject) => {
        timer = setTimeout(() => reject(new Error(timeoutMessage)), ms);
    });
    return Promise.race([promise, timeout]).finally(() => clearTimeout(timer));
}

async function initHandLandmarker() {
    let vision;
    try {
        vision = await withTimeout(
            FilesetResolver.forVisionTasks("https://cdn.jsdelivr.net/npm/@mediapipe/tasks-vision@0.10.14/wasm"),
            LOAD_TIMEOUT_MS, "Timeout loading MediaPipe (WASM)."
        );
        visionInstance = vision;
    } catch (err) {
        throw err;
    }

    let useGPU = false;
    try {
        const testCanvas = document.createElement("canvas");
        const gl = testCanvas.getContext("webgl") || testCanvas.getContext("experimental-webgl");
        if (gl) useGPU = true;
    } catch (e) {
        useGPU = false;
    }

    if (useGPU) {
        try {
            return await withTimeout(
                HandLandmarker.createFromOptions(vision, {
                    baseOptions: {
                        modelAssetPath: "https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task",
                        delegate: "GPU"
                    },
                    runningMode: "video",
                    numHands: 2,
                    minHandDetectionConfidence: 0.6,
                    minHandPresenceConfidence: 0.6,
                    minTrackingConfidence: 0.6,
                }), LOAD_TIMEOUT_MS, "Timeout downloading HandLandmarker model GPU."
            );
        } catch (gpuErr) {
            console.warn("GPU failed, retrying CPU...");
        }
    }

    return await withTimeout(
        HandLandmarker.createFromOptions(vision, {
            baseOptions: {
                modelAssetPath: "https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task",
                delegate: "CPU"
            },
            runningMode: "video",
            numHands: 2,
            minHandDetectionConfidence: 0.6,
            minHandPresenceConfidence: 0.6,
            minTrackingConfidence: 0.6,
        }), LOAD_TIMEOUT_MS, "Timeout downloading HandLandmarker model CPU."
    );
}

async function fallbackToCPU() {
    if (isFallbackActive) return;
    isFallbackActive = true;
    statusText.value = "WebGL error, switching to CPU...";
    try {
        handLandmarker = null;
        handLandmarker = await withTimeout(
            HandLandmarker.createFromOptions(visionInstance, {
                baseOptions: {
                    modelAssetPath: "https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task",
                    delegate: "CPU"
                },
                runningMode: "video",
                numHands: 2,
                minHandDetectionConfidence: 0.6,
                minHandPresenceConfidence: 0.6,
                minTrackingConfidence: 0.6,
            }), LOAD_TIMEOUT_MS, "Timeout CPU fallback."
        );
        statusText.value = "Connected (CPU Fallback)";
    } catch (err) {
        statusText.value = "Fallback Failed";
    } finally {
        isFallbackActive = false;
    }
}

// ==========================================
// 4. MAIN LOOP & RENDERING
// ==========================================

function renderLoop() {
    if (!loopRunning) return;
    const activeStates = ["tracking", "countdown", "puzzle", "shattering"];

    if (activeStates.includes(appState.value) && videoEl.value?.readyState >= 2) {
        drawVideoFrame();

        if (handLandmarker) {
            const nowMs = performance.now();
            if (nowMs - lastDetectTime >= 60) {
                lastDetectTime = nowMs;
                try {
                    const result = handLandmarker.detectForVideo(videoEl.value, nowMs);
                    currentLandmarks = result.landmarks || [];
                    currentHandedness = result.handedness || [];
                } catch (err) {
                    if (err.message && (err.message.includes("activeTexture") || err.message.includes("WebGL"))) {
                        fallbackToCPU();
                    }
                }
            }
            processResults({
                landmarks: currentLandmarks,
                handedness: currentHandedness
            });
        }
    }
    requestAnimationFrame(renderLoop);
}

function processResults(result) {
    if (appState.value === "shattering") {
        updateAndDrawShatter();
        statusText.value = "saving…";
        return;
    }

    const handsLandmarks = result.landmarks || [];
    const noHands = handsLandmarks.length === 0;

    if (noHands) {
        statusDotClass.value = puzzle.solved ? "bg-emerald-400 drop-shadow-[0_0_10px_rgba(95,174,110,1)]" : "bg-rose-400";
        fistHoldCounter = 0;
        freezeGate.holding = false;

        if (drag.activeHand && drag.piece) handleDragForHand(drag.activeHand, false, {
            x: drag.piece.x,
            y: drag.piece.y
        });

        if (appState.value === "tracking") {
            const sinceLastSeen = performance.now() - lastSeenFrame.at;
            if (lastSeenFrame.box && sinceLastSeen < FRAME_GRACE_MS) {
                applyBWInsideBox(lastSeenFrame.box);
                drawLiveFrameOverlay(lastSeenFrame.box);
            }
            statusText.value = isStripFull() ? "gallery full - reset to continue" : "searching for hands…";
            return;
        }

        if (appState.value === "countdown") {
            drawCountdownOverlay(puzzle.boardBox);
            return;
        }

        if (appState.value === "puzzle") {
            puzzle.solved = reconcilePlacedState(puzzle.boardBox, puzzle.tileW, puzzle.tileH);
            drawBoardAndPieces();
            statusText.value = shatter.active ? "puzzle solved!" : "assemble puzzle using pinch gesture";
        }
        return;
    }

    statusDotClass.value = puzzle.solved ? "bg-emerald-400 drop-shadow-[0_0_10px_rgba(95,174,110,1)]" : "bg-emerald-400";

    const anyFist = handsLandmarks.some(isFist);
    const draggingNow = drag.activeHand !== null && drag.piece !== null;

    if (anyFist && !draggingNow && appState.value !== "tracking") {
        fistHoldCounter++;
        if (fistHoldCounter >= FIST_HOLD_FRAMES) {
            fistHoldCounter = 0;
            handleFistReset();
            return;
        }
    } else {
        fistHoldCounter = 0;
    }

    if (appState.value === "tracking") {
        if (isStripFull()) {
            statusText.value = "gallery full — download to continue";
            return;
        }

        if (handsLandmarks.length === 2) {
            const [handA, handB] = handsLandmarks;
            const indexA = mirrorLandmarkX(handA[LM.INDEX_TIP]);
            const indexB = mirrorLandmarkX(handB[LM.INDEX_TIP]);
            const frameBox = computeHandFrame(indexA, indexB);

            if (frameBox.width > 4 && frameBox.height > 4) {
                applyBWInsideBox(frameBox);
                drawLiveFrameOverlay(frameBox);
                lastSeenFrame.box = frameBox;
                lastSeenFrame.at = performance.now();
            }

            const bothPinching = isPinching(handA) && isPinching(handB);
            if (bothPinching && frameBox.width > 40 && frameBox.height > 40) {
                if (!freezeGate.holding) {
                    freezeGate.holding = true;
                    freezeGate.since = performance.now();
                }
                if (!countdown.active) statusText.value = "hold pinch gesture…";
                statusDotClass.value = "bg-rose-500 drop-shadow-[0_0_8px_rgba(224,83,61,1)]";

                if (performance.now() - freezeGate.since > FREEZE_HOLD_MS) {
                    freezeGate.holding = false;
                    startCountdown(frameBox);
                }
            } else {
                freezeGate.holding = false;
                statusText.value = "hand detected";
            }
        } else {
            freezeGate.holding = false;
            const sinceLastSeen = performance.now() - lastSeenFrame.at;
            if (lastSeenFrame.box && sinceLastSeen < FRAME_GRACE_MS) {
                applyBWInsideBox(lastSeenFrame.box);
                drawLiveFrameOverlay(lastSeenFrame.box);
                statusText.value = "hand detected";
            } else {
                statusText.value = "searching for hand";
            }
        }
        return;
    }

    if (appState.value === "countdown") {
        drawCountdownOverlay(puzzle.boardBox);
        return;
    }

    if (appState.value === "puzzle") {
        const labelsPresent = new Set();
        handsLandmarks.forEach((lm, i) => {
            const label = result.handedness[i] && result.handedness[i][0] ? result.handedness[i][0].categoryName : (i === 0 ? "Left" : "Right");
            labelsPresent.add(label);
            handleDragForHand(label, isPinching(lm), toPixel(mirrorLandmarkX(lm[LM.INDEX_TIP])));
        });

        if (drag.activeHand && !labelsPresent.has(drag.activeHand) && drag.piece) {
            handleDragForHand(drag.activeHand, false, {
                x: drag.piece.x,
                y: drag.piece.y
            });
        }

        if (!drag.piece) puzzle.solved = reconcilePlacedState(puzzle.boardBox, puzzle.tileW, puzzle.tileH);

        drawBoardAndPieces();
        drawHandSkeletonsOverBoard(handsLandmarks, puzzle.boardBox);

        statusText.value = puzzle.solved ?
            (fistHoldCounter > 0 ? `saving… hold fist (${fistHoldCounter}/${FIST_HOLD_FRAMES})` : "puzzle solved! clench fist to save") :
            "assemble puzzle using pinch gesture";
    }
}

// ==========================================
// 5. MATH & GESTURE UTILS
// ==========================================

function dist2D(a, b) {
    return Math.sqrt(Math.pow(a.x - b.x, 2) + Math.pow(a.y - b.y, 2));
}

function isPinching(lm) {
    return dist2D(lm[LM.THUMB_TIP], lm[LM.INDEX_TIP]) < PINCH_THRESHOLD;
}

function isFist(lm) {
    const w = lm[LM.WRIST];
    let curled = 0;
    [
        [LM.INDEX_TIP, LM.INDEX_MCP],
        [LM.MIDDLE_TIP, LM.MIDDLE_MCP],
        [LM.RING_TIP, LM.RING_MCP],
        [LM.PINKY_TIP, LM.PINKY_MCP]
    ].forEach(([tip, mcp]) => {
        if (dist2D(lm[tip], w) < dist2D(lm[mcp], w)) curled++;
    });
    return curled >= 4;
}

function toPixel(lm) {
    return {
        x: lm.x * sceneCanvas.value.width,
        y: lm.y * sceneCanvas.value.height
    };
}

function mirrorLandmarkX(lm) {
    return {
        x: 1 - lm.x,
        y: lm.y
    };
}

function getFilterString() {
    if (config.filter === 'bw') return 'grayscale(100%) contrast(120%)';
    if (config.filter === 'vintage') return 'sepia(50%) contrast(120%) saturate(80%)';
    return 'none';
}

function computeHandFrame(indexA, indexB) {
    const a = toPixel(indexA),
        b = toPixel(indexB);
    const x = Math.max(0, Math.min(a.x, b.x) - FRAME_PADDING);
    const y = Math.max(0, Math.min(a.y, b.y) - FRAME_PADDING);
    const width = Math.min(sceneCanvas.value.width, Math.max(a.x, b.x) + FRAME_PADDING) - x;
    const height = Math.min(sceneCanvas.value.height, Math.max(a.y, b.y) + FRAME_PADDING) - y;
    return {
        x,
        y,
        width,
        height
    };
}

// ==========================================
// 6. PUZZLE CORE & ANIMATION
// ==========================================

function startCountdown(box) {
    puzzle.boardBox = {
        ...box
    };
    appState.value = "countdown";
    countdown.active = true;
    countdown.startedAt = performance.now();
}

function finishCountdownAndCapture(box) {
    countdown.active = false;
    const cw = sceneCanvas.value.width,
        ch = sceneCanvas.value.height;

    const mirroredFrame = document.createElement("canvas");
    mirroredFrame.width = cw;
    mirroredFrame.height = ch;
    const mCtx = mirroredFrame.getContext("2d");
    mCtx.translate(cw, 0);
    mCtx.scale(-1, 1);
    mCtx.filter = getFilterString();
    mCtx.drawImage(videoEl.value, 0, 0, cw, ch);

    const cropCanvas = document.createElement("canvas");
    cropCanvas.width = Math.max(1, Math.round(box.width));
    cropCanvas.height = Math.max(1, Math.round(box.height));
    cropCanvas.getContext("2d").drawImage(mirroredFrame, box.x, box.y, box.width, box.height, 0, 0, cropCanvas.width, cropCanvas.height);

    puzzle.fullPhotoboothCanvas = cropCanvas;
    const tileW = Math.floor(cropCanvas.width / config.grid);
    const tileH = Math.floor(cropCanvas.height / config.grid);
    const pieces = [];
    const slots = [];

    for (let row = 0; row < config.grid; row++) {
        for (let col = 0; col < config.grid; col++) {
            const sx = col * tileW,
                sy = row * tileH;
            const w = col === config.grid - 1 ? cropCanvas.width - sx : tileW;
            const h = row === config.grid - 1 ? cropCanvas.height - sy : tileH;

            const pCanvas = document.createElement("canvas");
            pCanvas.width = w;
            pCanvas.height = h;
            pCanvas.getContext("2d").drawImage(cropCanvas, sx, sy, w, h, 0, 0, w, h);
            pieces.push({
                row,
                col,
                canvas: pCanvas,
                w,
                h,
                x: 0,
                y: 0,
                placed: false,
                dragging: false
            });
            slots.push({
                x: box.x + col * tileW,
                y: box.y + row * tileH
            });
        }
    }

    for (let i = slots.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [slots[i], slots[j]] = [slots[j], slots[i]];
    }

    pieces.forEach((piece, i) => {
        piece.x = slots[i].x;
        piece.y = slots[i].y;
        if (isNearOwnCell(piece, box, tileW, tileH)) snapPieceToCell(piece, box, tileW, tileH);
    });

    puzzle.boardBox = box;
    puzzle.pieces = pieces;
    puzzle.tileW = tileW;
    puzzle.tileH = tileH;
    puzzle.solved = pieces.every((p) => p.placed);
    appState.value = "puzzle";
    fistHoldCounter = 0;
}

function handleDragForHand(handLabel, pinching, indexPx) {
    if (pinching) {
        if (!drag.activeHand) {
            let best = null,
                bestDist = Infinity;
            for (const p of puzzle.pieces) {
                if (p.displacing) continue;
                const d = Math.hypot(indexPx.x - (p.x + p.w / 2), indexPx.y - (p.y + p.h / 2));
                if (d < Math.max(p.w, p.h) * 0.75 && d < bestDist) {
                    best = p;
                    bestDist = d;
                }
            }
            if (best) {
                drag.activeHand = handLabel;
                drag.piece = best;
                drag.offsetX = indexPx.x - best.x;
                drag.offsetY = indexPx.y - best.y;
                best.dragging = true;
                best.placed = false;
            }
        } else if (drag.activeHand === handLabel && drag.piece) {
            drag.piece.x = indexPx.x - drag.offsetX;
            drag.piece.y = indexPx.y - drag.offsetY;
        }
    } else if (drag.activeHand === handLabel && drag.piece) {
        const p = drag.piece;
        p.dragging = false;
        if (isNearOwnCell(p, puzzle.boardBox, puzzle.tileW, puzzle.tileH)) {
            snapPieceToCell(p, puzzle.boardBox, puzzle.tileW, puzzle.tileH);
        } else {
            const dropCol = Math.min(config.grid - 1, Math.max(0, Math.floor((p.x + p.w / 2 - puzzle.boardBox.x) / puzzle.tileW)));
            const dropRow = Math.min(config.grid - 1, Math.max(0, Math.floor((p.y + p.h / 2 - puzzle.boardBox.y) / puzzle.tileH)));
            p.x = puzzle.boardBox.x + dropCol * puzzle.tileW;
            p.y = puzzle.boardBox.y + dropRow * puzzle.tileH;
            p.placed = (dropCol === p.col && dropRow === p.row);
            displaceCellOccupant(p, dropRow, dropCol, puzzle.boardBox, puzzle.tileW, puzzle.tileH);
        }
        drag.activeHand = null;
        drag.piece = null;
        puzzle.solved = reconcilePlacedState(puzzle.boardBox, puzzle.tileW, puzzle.tileH);
    }
}

function isNearOwnCell(p, box, tw, th) {
    return Math.hypot(p.x - (box.x + p.col * tw), p.y - (box.y + p.row * th)) < Math.min(tw, th) * SNAP_DISTANCE_RATIO;
}

function reconcilePlacedState(box, tw, th) {
    if (!box || !puzzle.pieces.length) return false;
    puzzle.pieces.forEach(p => {
        if (!p.displacing && !p.dragging) p.placed = isNearOwnCell(p, box, tw, th);
    });
    return puzzle.pieces.every(p => p.placed);
}

function snapPieceToCell(p, box, tw, th) {
    displaceCellOccupant(p, p.row, p.col, box, tw, th);
    p.x = box.x + p.col * tw;
    p.y = box.y + p.row * th;
    p.placed = true;
}

function displaceCellOccupant(piece, tRow, tCol, box, tw, th) {
    const cx = box.x + tCol * tw,
        cy = box.y + tRow * th;
    const occupant = puzzle.pieces.find(p => p !== piece && !p.displacing && (p.x + p.w / 2 >= cx && p.x + p.w / 2 < cx + tw && p.y + p.h / 2 >= cy && p.y + p.h / 2 < cy + th));
    if (!occupant || (occupant.row === tRow && occupant.col === tCol && occupant.placed)) return;

    occupant.placed = false;
    const freeCells = [];
    for (let r = 0; r < config.grid; r++) {
        for (let c = 0; c < config.grid; c++) {
            if (r === tRow && c === tCol) continue;
            const tx = box.x + c * tw,
                ty = box.y + r * th;
            if (!puzzle.pieces.some(p => p !== occupant && p !== piece && !p.displacing && p.x + p.w / 2 >= tx && p.x + p.w / 2 < tx + tw && p.y + p.h / 2 >= ty && p.y + p.h / 2 < ty + th)) {
                freeCells.push({
                    row: r,
                    col: c
                });
            }
        }
    }
    const target = freeCells.length > 0 ? freeCells[Math.floor(Math.random() * freeCells.length)] : {
        row: occupant.row,
        col: occupant.col
    };
    animateDisplacement(occupant, box.x + target.col * tw, box.y + target.row * th);
}

function animateDisplacement(p, tx, ty) {
    const sx = p.x,
        sy = p.y,
        startAt = performance.now();
    p.displacing = true;

    function step() {
        const t = Math.min(1, (performance.now() - startAt) / DISPLACE_ANIM_MS);
        const eased = 1 - Math.pow(1 - t, 3);
        p.x = sx + (tx - sx) * eased;
        p.y = sy + (ty - sy) * eased;
        if (t < 1) requestAnimationFrame(step);
        else {
            p.x = tx;
            p.y = ty;
            p.displacing = false;
            p.x = Math.min(Math.max(p.x, puzzle.boardBox.x), puzzle.boardBox.x + puzzle.boardBox.width - p.w);
            p.y = Math.min(Math.max(p.y, puzzle.boardBox.y), puzzle.boardBox.y + puzzle.boardBox.height - p.h);
        }
    }
    requestAnimationFrame(step);
}

function handleFistReset() {
    if (appState.value !== "puzzle") {
        resetPuzzleOnly();
        return;
    }
    if (reconcilePlacedState(puzzle.boardBox, puzzle.tileW, puzzle.tileH) && puzzle.fullPhotoboothCanvas) {
        shatter.pendingCanvas = puzzle.fullPhotoboothCanvas;
        startShatter(puzzle.fullPhotoboothCanvas, puzzle.boardBox);
    } else {
        resetPuzzleOnly();
    }
}

function resetPuzzleOnly() {
    puzzle.boardBox = null;
    puzzle.pieces = [];
    puzzle.solved = false;
    puzzle.fullPhotoboothCanvas = null;
    appState.value = "tracking";
    countdown.active = false;
    drag.activeHand = null;
    drag.piece = null;
    shatter.active = false;
    shatter.fragments = [];
    shatter.pendingCanvas = null;
    fistHoldCounter = 0;
    lastSeenFrame.box = null;
    lastSeenFrame.at = 0;
}

// ==========================================
// 7. CANVAS DRAWING ROUTINES
// ==========================================

function drawVideoFrame() {
    const ctx = sceneCanvas.value.getContext('2d');
    ctx.save();
    ctx.translate(sceneCanvas.value.width, 0);
    ctx.scale(-1, 1);
    ctx.drawImage(videoEl.value, 0, 0, sceneCanvas.value.width, sceneCanvas.value.height);
    ctx.restore();
}

function applyBWInsideBox(box) {
    const ctx = sceneCanvas.value.getContext('2d');
    ctx.save();
    ctx.beginPath();
    ctx.rect(box.x, box.y, box.width, box.height);
    ctx.clip();
    ctx.filter = getFilterString();
    ctx.translate(sceneCanvas.value.width, 0);
    ctx.scale(-1, 1);
    ctx.drawImage(videoEl.value, 0, 0, sceneCanvas.value.width, sceneCanvas.value.height);
    ctx.restore();
}

function drawLiveFrameOverlay(box) {
    const ctx = sceneCanvas.value.getContext('2d');
    ctx.save();
    ctx.strokeStyle = "#f5c518";
    ctx.lineWidth = 3;
    ctx.strokeRect(box.x, box.y, box.width, box.height);
    const cornerLen = 18;
    ctx.lineWidth = 4;
    [
        [1, 1],
        [-1, 1],
        [1, -1],
        [-1, -1]
    ].forEach(([dx, dy]) => {
        const cx = dx > 0 ? box.x : box.x + box.width,
            cy = dy > 0 ? box.y : box.y + box.height;
        ctx.beginPath();
        ctx.moveTo(cx, cy + cornerLen * dy);
        ctx.lineTo(cx, cy);
        ctx.lineTo(cx + cornerLen * dx, cy);
        ctx.stroke();
    });
    ctx.restore();
}

function drawCountdownOverlay(box) {
    const ctx = sceneCanvas.value.getContext('2d');
    const elapsed = (performance.now() - countdown.startedAt) / 1000;
    const remaining = COUNTDOWN_SECONDS - elapsed;
    if (remaining <= 0) {
        finishCountdownAndCapture(box);
        return;
    }

    applyBWInsideBox(box);
    ctx.save();
    ctx.strokeStyle = "#f5c518";
    ctx.lineWidth = 3;
    ctx.strokeRect(box.x, box.y, box.width, box.height);
    ctx.fillStyle = "rgba(10,10,8,0.45)";
    ctx.fillRect(box.x, box.y, box.width, box.height);
    ctx.font = `${Math.max(48, Math.min(box.width, box.height) * 0.4)}px 'IBM Plex Mono', monospace`;
    ctx.fillStyle = "#f5c518";
    ctx.textAlign = "center";
    ctx.textBaseline = "middle";
    ctx.fillText(String(Math.ceil(remaining)), box.x + box.width / 2, box.y + box.height / 2);
    ctx.restore();
    statusText.value = `taking picture in ${Math.ceil(remaining)}…`;
}

function drawBoardAndPieces() {
    const ctx = sceneCanvas.value.getContext('2d');
    const box = puzzle.boardBox;
    ctx.save();
    ctx.fillStyle = "rgba(0, 0, 0, 0.15)";
    ctx.fillRect(box.x, box.y, box.width, box.height);
    ctx.strokeStyle = "rgba(0, 0, 0, 0.3)";
    ctx.lineWidth = 1;
    ctx.setLineDash([5, 5]);
    for (let r = 0; r < config.grid; r++)
        for (let c = 0; c < config.grid; c++) ctx.strokeRect(box.x + c * puzzle.tileW, box.y + r * puzzle.tileH, puzzle.tileW, puzzle.tileH);
    ctx.restore();

    [...puzzle.pieces].sort((a, b) => (a.dragging ? 1 : 0) - (b.dragging ? 1 : 0)).forEach(p => {
        ctx.save();
        if (p.dragging) {
            ctx.shadowColor = "rgba(245,197,24,0.9)";
            ctx.shadowBlur = 14;
        }
        ctx.drawImage(p.canvas, p.x, p.y, p.w, p.h);
        ctx.strokeStyle = p.placed ? "#5fae6e" : "rgba(234,229,214,0.5)";
        ctx.lineWidth = p.dragging ? 3 : 1.5;
        ctx.strokeRect(p.x, p.y, p.w, p.h);
        ctx.restore();
    });

    ctx.save();
    ctx.strokeStyle = puzzle.solved ? "#5fae6e" : "#f5c518";
    ctx.lineWidth = 3;
    ctx.strokeRect(box.x, box.y, box.width, box.height);
    ctx.restore();
    if (puzzle.solved) {
        ctx.save();
        ctx.fillStyle = "rgba(95,174,110,0.15)";
        ctx.fillRect(box.x, box.y, box.width, box.height);
        ctx.restore();
    }
}

function drawHandSkeletonsOverBoard(hands, box) {
    const ctx = sceneCanvas.value.getContext('2d');
    hands.forEach(lm => {
        const pxs = lm.map(pt => toPixel(mirrorLandmarkX(pt)));
        if (pxs.some(p => p.x >= box.x && p.x <= box.x + box.width && p.y >= box.y && p.y <= box.y + box.height)) {
            ctx.save();
            ctx.lineCap = "round";
            ctx.lineJoin = "round";
            ctx.shadowColor = "rgba(255,255,255,0.85)";
            ctx.shadowBlur = 10;
            ctx.strokeStyle = "white";
            ctx.lineWidth = 3;
            HAND_CONNECTIONS.forEach(([a, b]) => {
                ctx.beginPath();
                ctx.moveTo(pxs[a].x, pxs[a].y);
                ctx.lineTo(pxs[b].x, pxs[b].y);
                ctx.stroke();
            });
            ctx.shadowBlur = 6;
            ctx.fillStyle = "white";
            pxs.forEach(p => {
                ctx.beginPath();
                ctx.arc(p.x, p.y, 3.2, 0, Math.PI * 2);
                ctx.fill();
            });
            ctx.restore();
        }
    });
}

function startShatter(src, box) {
    const cols = config.grid * 2,
        rows = config.grid * 2,
        fw = src.width / cols,
        fh = src.height / rows,
        frags = [];
    for (let r = 0; r < rows; r++)
        for (let c = 0; c < cols; c++) {
            const sx = c * fw,
                sy = r * fh,
                fc = document.createElement("canvas");
            fc.width = Math.ceil(fw);
            fc.height = Math.ceil(fh);
            fc.getContext("2d").drawImage(src, sx, sy, fw, fh, 0, 0, fc.width, fc.height);
            const dirX = (box.x + sx + fw / 2) - (box.x + box.width / 2),
                dirY = (box.y + sy + fh / 2) - (box.y + box.height / 2),
                dl = Math.max(1, Math.hypot(dirX, dirY)),
                s = 90 + Math.random() * 160;
            frags.push({
                canvas: fc,
                x: box.x + sx + fw / 2,
                y: box.y + sy + fh / 2,
                w: fw,
                h: fh,
                vx: (dirX / dl) * s + (Math.random() - 0.5) * 40,
                vy: (dirY / dl) * s + (Math.random() - 0.5) * 40 - 60,
                rotation: 0,
                rotationSpeed: (Math.random() - 0.5) * 6,
                gravity: 220 + Math.random() * 80
            });
        }
    shatter.fragments = frags;
    shatter.active = true;
    shatter.startedAt = performance.now();
    appState.value = "shattering";
}

function updateAndDrawShatter() {
    const t = Math.min(1, (performance.now() - shatter.startedAt) / SHATTER_DURATION_MS),
        dt = 1 / 60,
        ctx = sceneCanvas.value.getContext('2d');
    if (t >= 1) {
        shatter.active = false;
        shatter.fragments = [];
        if (shatter.pendingCanvas) addToGallery(shatter.pendingCanvas);
        shatter.pendingCanvas = null;
        if (appState.value !== "edit_photo") resetPuzzleOnly();
        return;
    }
    ctx.save();
    shatter.fragments.forEach(f => {
        f.x += f.vx * dt;
        f.y += f.vy * dt;
        f.vy += f.gravity * dt;
        f.rotation += f.rotationSpeed * dt;
        ctx.save();
        ctx.globalAlpha = t < 0.45 ? 1 : Math.max(0, 1 - (t - 0.45) / 0.55);
        ctx.translate(f.x, f.y);
        ctx.rotate(f.rotation);
        ctx.scale(1 - t * 0.25, 1 - t * 0.25);
        ctx.drawImage(f.canvas, -f.w / 2, -f.h / 2, f.w, f.h);
        ctx.restore();
    });
    ctx.restore();
}

// ==========================================
// 8. GALLERY & EDITING
// ==========================================

function isStripFull() {
    return galleryEntries.value.length >= config.layout;
}

function addToGallery(snap) {
    if (isStripFull()) return;
    galleryEntries.value.push({
        canvas: snap,
        time: Date.now()
    });

    if (isStripFull()) {
        const stripCanvas = createPhotoStripCanvas();
        if (stripCanvas) {
            currentEditCanvas = stripCanvas;
            appState.value = "printing";
            printingImageSrc.value = stripCanvas.toDataURL("image/png");

            requestAnimationFrame(() => requestAnimationFrame(() => isPrintingAnimated.value = true));
            setTimeout(() => {
                appState.value = "edit_photo";
                setTimeout(() => {
                    editCanvas.value.width = currentEditCanvas.width;
                    editCanvas.value.height = currentEditCanvas.height;
                    redrawEditCanvas();
                }, 100);
            }, 3500);
        }
    }
}

function createPhotoStripCanvas() {
    if (galleryEntries.value.length === 0) return null;
    const tw = galleryEntries.value[0].canvas.width;
    const heights = galleryEntries.value.map(e => Math.round(e.canvas.height * (tw / e.canvas.width)));
    const sc = document.createElement("canvas");
    sc.width = tw + 48;
    sc.height = 24 + 120 + heights.reduce((a, b) => a + b, 0) + 16 * (galleryEntries.value.length - 1);
    const ctx = sc.getContext("2d");
    let cy = 24;
    galleryEntries.value.forEach((e, i) => {
        ctx.drawImage(e.canvas, 24, cy, tw, heights[i]);
        cy += heights[i] + 16;
    });
    return sc;
}

function setBorderColor(c) {
    currentBorderColor.value = c;
    redrawEditCanvas();
}

function addSticker(e) {
    placedStickers.push({
        emoji: e,
        x: editCanvas.value.width / 2 + (Math.random() - 0.5) * 200,
        y: editCanvas.value.height / 2 + (Math.random() - 0.5) * 200,
        size: 80
    });
    redrawEditCanvas();
}

function redrawEditCanvas() {
    if (!currentEditCanvas || !editCanvas.value) return;
    const ctx = editCanvas.value.getContext("2d");
    ctx.clearRect(0, 0, editCanvas.value.width, editCanvas.value.height);
    ctx.fillStyle = currentBorderColor.value;
    ctx.fillRect(0, 0, editCanvas.value.width, editCanvas.value.height);
    ctx.drawImage(currentEditCanvas, 0, 0);
    ctx.textAlign = "center";
    ctx.textBaseline = "middle";
    placedStickers.forEach(s => {
        ctx.font = `${s.size}px "Material Symbols Outlined"`;
        ctx.fillText(s.emoji, s.x, s.y);
    });
}

function getCanvasPointer(e) {
    const rect = editCanvas.value.getBoundingClientRect();
    const cx = e.touches ? e.touches[0].clientX : e.clientX,
        cy = e.touches ? e.touches[0].clientY : e.clientY;
    const cr = editCanvas.value.width / editCanvas.value.height,
        rr = rect.width / rect.height;
    let dw = rect.width,
        dh = rect.height,
        ox = 0,
        oy = 0;
    if (cr > rr) {
        dh = rect.width / cr;
        oy = (rect.height - dh) / 2;
    } else {
        dw = rect.height * cr;
        ox = (rect.width - dw) / 2;
    }
    return {
        x: (cx - rect.left - ox) * (editCanvas.value.width / dw),
        y: (cy - rect.top - oy) * (editCanvas.value.height / dh),
        cx,
        cy
    };
}

function handleDragStart(e) {
    if (appState.value !== "edit_photo") return;
    const ptr = getCanvasPointer(e);
    for (let i = placedStickers.length - 1; i >= 0; i--) {
        const s = placedStickers[i];
        if (Math.abs(ptr.x - s.x) < s.size * 0.6 && Math.abs(ptr.y - s.y) < s.size * 0.6) {
            draggingStickerIndex = i;
            dragOffsetX = s.x - ptr.x;
            dragOffsetY = s.y - ptr.y;
            isHoveringTrash.value = false;
            e.preventDefault();
            return;
        }
    }
}

function handleDragMove(e) {
    if (draggingStickerIndex === -1) return;
    e.preventDefault();
    const ptr = getCanvasPointer(e);
    placedStickers[draggingStickerIndex].x = ptr.x + dragOffsetX;
    placedStickers[draggingStickerIndex].y = ptr.y + dragOffsetY;

    if (trashBin.value) {
        const tr = trashBin.value.getBoundingClientRect();
        isHoveringTrash.value = (ptr.cx >= tr.left && ptr.cx <= tr.right && ptr.cy >= tr.top && ptr.cy <= tr.bottom);
    }
    redrawEditCanvas();
}

function handleDragEnd(e) {
    if (draggingStickerIndex === -1) return;
    const cx = e.changedTouches ? e.changedTouches[0].clientX : e.clientX,
        cy = e.changedTouches ? e.changedTouches[0].clientY : e.clientY;
    if (trashBin.value) {
        const tr = trashBin.value.getBoundingClientRect();
        if (cx >= tr.left && cx <= tr.right && cy >= tr.top && cy <= tr.bottom) placedStickers.splice(draggingStickerIndex, 1);
    }
    draggingStickerIndex = -1;
    isHoveringTrash.value = false;
    redrawEditCanvas();
}

function finishEditAndReturn(save) {
    if (save && currentEditCanvas) {
        const fc = document.createElement("canvas");
        fc.width = editCanvas.value.width;
        fc.height = editCanvas.value.height;
        fc.getContext("2d").drawImage(editCanvas.value, 0, 0);
        const l = document.createElement("a");
        l.download = `scrapbook-image-${Date.now()}.png`;
        l.href = fc.toDataURL("image/png");
        l.click();
    }
    placedStickers = [];
    currentEditCanvas = null;
    isPrintingAnimated.value = false;
    galleryEntries.value = [];
    resetPuzzleOnly();
    appState.value = "welcome";
}

// ==========================================
// 9. LIFECYCLE HOOKS
// ==========================================

onMounted(() => {
    window.addEventListener("mousemove", handleDragMove);
    window.addEventListener("touchmove", handleDragMove, {
        passive: false
    });
    window.addEventListener("mouseup", handleDragEnd);
    window.addEventListener("touchend", handleDragEnd);
});

onUnmounted(() => {
    window.removeEventListener("mousemove", handleDragMove);
    window.removeEventListener("touchmove", handleDragMove);
    window.removeEventListener("mouseup", handleDragEnd);
    window.removeEventListener("touchend", handleDragEnd);
});
</script>

<style scoped>
.app-root {
    display: flex;
    width: 100dvw;
    height: 100dvh;
    animation: fadeIn 0.5s ease-out forwards;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.polaroid {
    background: white;
    padding: 10px 10px 40px 10px;
    box-shadow: 2px 4px 15px rgba(0, 0, 0, 0.1);
    border: 1px solid #e5e7eb;
}

.washi-tape {
    background-image: repeating-linear-gradient(
        45deg,
        rgba(255, 255, 255, 0.4),
        rgba(255, 255, 255, 0.4) 10px,
        rgba(0, 0, 0, 0.05) 10px,
        rgba(0, 0, 0, 0.05) 20px
    );
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    opacity: 0.85;
}

.washi-pink { background-color: #fecaca; }
.washi-yellow { background-color: #fef08a; }
.washi-blue { background-color: #bfdbfe; }
.washi-green { background-color: #bbf7d0; }

.stitched-border {
    border: 2px dashed #9ca3af;
    border-radius: 10px;
}

.cutout-shadow {
    box-shadow: 4px 4px 0 #292524;
    border: 2px solid #292524;
}

.animate-wiggle {
    animation: wiggle 3s ease-in-out infinite;
}

@keyframes wiggle {
    0%, 100% {
        transform: rotate(-2deg);
    }
    50% {
        transform: rotate(2deg);
    }
}

@media (max-width: 1440px) {
    header {
        top: 12px;
    }
    header > div {
        padding-top: 10px;
        padding-bottom: 10px;
    }
}
</style>
