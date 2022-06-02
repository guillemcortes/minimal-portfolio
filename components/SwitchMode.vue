<template>
    <button
        v-if="$colorMode.preference === 'dark'"
        class="flex h-auto w-auto items-center"
        @click="toggleMode('light')"
    >
        <svg
            class="h-8 fill-current text-gray-50 w-8"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
        >
            <path
                fill-rule="evenodd"
                d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464"
                clip-rule="evenodd"
            ></path>
        </svg>
    </button>
    <button v-else @click="toggleMode('dark')">
        <svg
            class="h-8 fill-current text-dark-900 w-8"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
        >
            <path
                d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"
            ></path>
        </svg>
    </button>
</template>

<script setup lang="ts">
const colorMode = useColorMode();

function toggleMode(mode: string) {
    colorMode.preference = mode;
}
</script>