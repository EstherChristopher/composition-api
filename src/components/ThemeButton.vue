<template>
    <button
    :class="{ 'dark-mode': settings.theme === 'dark' }"
    @click="toggleMode"
    >Switch to {{ oppositeTheme }} mode</button>
</template>

<script>
import { computed, inject } from 'vue'
export default {
    setup() {
        const settings = inject('settings')
        const oppositeTheme = computed(() =>
        settings.theme === 'dark' ? 'light' : 'dark'
        )
        const toggleMode = () => {
            settings.theme = oppositeTheme.value
        }
        return { settings, oppositeTheme, toggleMode }
    }
}
</script>