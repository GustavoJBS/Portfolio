<script lang="ts">
    import { defineComponent } from 'vue'

    export default defineComponent({
        data() {
            return {
                routes: [
                    {
                        name: 'aboutme',
                        icon: '/src/assets/svg/aboutme.svg'
                    },
                    {
                        name: 'works',
                        icon: '/src/assets/svg/works.svg'
                    },
                    {
                        name: 'education',
                        icon: '/src/assets/svg/education.svg'
                    }
                ]
            }
        }
    })
</script>

<template>
    <div class="fixed right-5 lg:right-16 bottom-5 lg:bottom-16">
        <div class="flex flex-col gap-5">
            <a 
                v-for="route in routes" 
                :href="`#${route.name}`"
                class="rounded-full bg-yellow-400 p-4 duration-300 cursor-pointer hover:opacity-70"
            >
                <img
                    class="w-5 h-5 lg:w-8 lg:h-8"
                    :src="route.icon" 
                    :alt="route.icon"
                />
            </a>
        </div>
    </div>
</template>