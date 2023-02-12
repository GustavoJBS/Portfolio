<script lang="ts">
    import { defineComponent } from 'vue'

    export default defineComponent({})
</script>

<template>
    <div class="flex w-full py-8 flex-col items-center" id="projects">
        <div class="m-auto w-full lg:max-w-4xl flex flex-col gap-2 text-athens-gray-100">
            <div class="flex flex-col lg:flex-row justify-between items-center w-full">
                <h1 class="text-4xl text-cod-gray-800 font-semibold">
                    Look at My
    
                    <div class="font-bold text-transparent bg-clip-text bg-gradient-to-l from-fuchsia-500 via-red-600 to-orange-400">
                        Projects.
                    </div>
                </h1>

                <p>
                    Many of this Projects I only developed and I don't maintain today
                </p>
            </div>
        </div>
    </div>
</template>