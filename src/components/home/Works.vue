<script lang="ts">
    import { defineComponent } from 'vue'

    export default defineComponent({
        data() {
            return {
                workHistory: [
                    {
                        title: 'Software Engineer',
                        company: 'DevSquad', 
                        dateRange: 'March 2022 - Current',
                        logo: '/src/assets/img/companies/devsquad.png',
                        skills: [
                            {
                                name: 'Laravel',
                                icon: 'laravel'
                            }
                        ]
                    },
                    {
                        title: 'FrontEnd Developer',
                        company: 'Risoluto / 4Effect ', 
                        dateRange: 'November 2021 - April 2022',
                        logo: '/src/assets/img/companies/risoluto.png',
                        skills: [
                            {
                                name: 'Angular',
                                icon: 'angular'
                            }
                        ]
                    },
                    {
                        title: 'FullStack Developer',
                        company: 'Simbiose Social', 
                        dateRange: 'February 2021 - March 2022',
                        logo: '/src/assets/img/companies/simbioseSocial.png',
                        skills: [
                            {
                                name: 'Laravel',
                                icon: 'laravel'
                            }
                        ]
                    },
                ]
            }
        },
    })
</script>

<template>
    <div class="flex w-full py-8 flex-col items-center" id="works">
        <div class="m-auto w-full lg:max-w-4xl text-center flex flex-col gap-2 justify-center items-center text-athens-gray-100">
            
            <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-l from-fuchsia-500 via-red-600 to-orange-400">
                Work Experience
            </h1> 

            <div class="flex w-full flex-col divide-y divide-athens-gray-300">
                <div 
                    v-for="work in workHistory" 
                    class="flex w-full divide-y-2 divide-athens-gray-300 flex-col"
                >
                    <div class="flex flex-col lg:flex-row py-8 w-full justify-between items-center">
    
                        <img 
                            class="h-40 max-w-[14rem] mb-4 object-contain" 
                            :src="work.logo" 
                            :alt="`${work.company} Company Logo`" 
                        />
    
                        <div class="flex flex-col w-full h-full text-start lg:text-end lg:justify-between">
                            <div class="flex flex-col gap-1">
                                <h1 class="text-2xl font-bold text-cod-gray-900">
                                    {{ work.company }}
                                </h1>
                                <h2 class="text-xl text-cod-gray-800 font-semibold">
                                    {{ work.title }}
                                </h2>
                            </div>
    
                            <h2 class="text-xl text-cod-gray-800 font-semibold">
                                {{ work.dateRange }}
                            </h2>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>