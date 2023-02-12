<script lang="ts">
    import { defineComponent } from 'vue'
    import ProfileImage from '@/assets/img/profile-image.png'
    import Linkedin from '@/assets/svg/linkedin.svg'
    import Telegram from '@/assets/svg/telegram.svg'

    export default defineComponent({
        data() {
            return {
                imgProfile: ProfileImage,
                description: `Over the last 4 years, I've worked with many clients and companies, from Startups to LLCs.<br> I am
                looking for New International Opportunities 🗺️`,
                socialMedias: [
                    {
                        name: 'Linkedin',
                        icon: Linkedin,
                        url: 'https://www.linkedin.com/in/gustavosilva-03/',
                    },
                    {
                        name: 'Telegram',
                        icon: Telegram,
                        url: 'https://t.me/Gustavo_JS',
                    }
                ],
                mailTo: `mailto:gjbs1903@gmail.com`,
            }
        }
    })
</script>

<template>
    <div class="flex w-full py-8" id="aboutme">
        <div class="m-auto w-full lg:max-w-4xl text-center flex flex-col gap-2 justify-center items-center text-athens-gray-100">
            <img 
                :src="imgProfile" 
                alt="Profile Image"
                class="rounded-full h-44 md:h-56 aspect-square"
            />

            <div class="flex gap-3">
                <a 
                    class="rounded-full bg-sky-400 p-3 cursor-pointer hover:opacity-70 duration-300"
                    v-for="socialMedia in socialMedias"
                    :href="socialMedia.url"
                    target="_blank"
                >
                    <img 
                        class="h-6 w-6"
                        :src="socialMedia.icon" 
                        :alt="socialMedia.name"
                    />
                </a>
            </div>

            <div class="text-2xl lg:text-5xl font-bold">
                <h1 class="text-transparent bg-clip-text bg-gradient-to-l from-fuchsia-500 via-red-600 to-orange-400">
                    Hello I'm Gustavo Silva,
                </h1>

                <div class="text-cod-gray-800">
                    A Curious and Creative Software Developer 💻
                </div>
            </div>
    
            <p 
                class="text-lg mt-3 text-cod-gray-800"
                v-html="description" 
            />
    
            <div class="flex flex-col sm:flex-row gap-4">
                <a 
                    :href="mailTo"
                    target="_blank"
                    class="flex w-full sm:w-fit m-auto p-4 rounded-full bg-athens-gray-200 text-cod-gray-600 font-semibold cursor-pointer hover:opacity-70 duration-300"
                >
                    Let's Work Together
                </a>
            </div>
        </div>
    </div>
</template>
