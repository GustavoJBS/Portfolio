<script lang="ts">
    import { defineComponent } from 'vue'
    import Devsquad from '@/assets/img/companies/devsquad.png' 
    import Risoluto from '@/assets/img/companies/risoluto.png' 
    import SimbioseSocial from '@/assets/img/companies/simbioseSocial.png' 

    import Laravel from '@/assets/svg/skills/laravel.svg' 
    import Angular from '@/assets/svg/skills/angular.svg' 
    import React from '@/assets/svg/skills/react.svg' 
    import Ionic from '@/assets/svg/skills/ionic.svg'
    import Vue from '@/assets/svg/skills/vue.svg'
    import Livewire from '@/assets/svg/skills/livewire.png'
    import MySql from '@/assets/svg/skills/mysql.svg'
    import PostgreSQL from '@/assets/svg/skills/postgresql.svg'
    import TailwindCSS from '@/assets/svg/skills/tailwind.svg'
    
    export default defineComponent({
        data() {
            return {
                workHistory: [
                    {
                        title: 'Software Engineer',
                        company: 'DevSquad', 
                        dateRange: 'March 2022 - Current',
                        logo: Devsquad,
                        skills: [
                            {
                                name: 'Laravel',
                                icon: Laravel
                            },
                            {
                                name: 'MySql',
                                icon: MySql
                            },
                            {
                                name: 'TailwindCSS',
                                icon: TailwindCSS
                            },
                            {
                                name: 'Livewire',
                                icon: Livewire
                            },
                            {
                                name: 'Vue',
                                icon: Vue
                            }
                        ]
                    },
                    {
                        title: 'FrontEnd Developer',
                        company: 'Risoluto / 4Effect ', 
                        dateRange: 'November 2021 - April 2022',
                        logo: Risoluto,
                        skills: [
                            {
                                name: 'Angular',
                                icon: Angular
                            },
                            {
                                name: 'Ionic',
                                icon: Ionic
                            },
                            {
                                name: 'PostgreSQL',
                                icon: PostgreSQL
                            }
                        ]
                    },
                    {
                        title: 'FullStack Developer',
                        company: 'Simbiose Social', 
                        dateRange: 'February 2021 - March 2022',
                        logo: SimbioseSocial,
                        skills: [
                            {
                                name: 'Laravel',
                                icon: Laravel
                            },
                            {
                                name: 'React',
                                icon: React
                            },
                            {
                                name: 'MySql',
                                icon: MySql
                            },
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
                    <div class="flex flex-col lg:flex-row py-8 w-full justify-between items-center lg:items-start">
    
                        <img 
                            class="h-40 max-w-[14rem] mb-4 object-contain aspect-square" 
                            :src="work.logo" 
                            :alt="`${work.company} Company Logo`" 
                        />

                        <div class="grid gap-4 my-4 lg:ml-8 lg:my-0 w-full grid-cols-2">
                            <div 
                                v-for="skill in work.skills"
                                class="flex gap-2 items-center text-cod-gray-900"
                            >
                                <img 
                                    :src="skill.icon" 
                                    :alt="skill.name"
                                    class="w-8"
                                />

                                <h3 class="text-lg text-cod-gray-800 font-semibold">
                                    {{ skill.name }}
                                </h3>
                            </div>
                        </div>
    
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