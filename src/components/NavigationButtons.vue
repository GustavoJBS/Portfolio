<script lang="ts">
    import { defineComponent } from 'vue'
    import AboutMe from '@/assets/svg/aboutme.svg'
    import Works from '@/assets/svg/works.svg'
    import Education from '@/assets/svg/aboutme.svg'

    export default defineComponent({
        data() {
            return {
                routes: [
                    {
                        name: 'aboutme',
                        icon: AboutMe
                    },
                    {
                        name: 'works',
                        icon: Works
                    },
                    {
                        name: 'education',
                        icon: Education
                    }
                ]
            }
        },
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