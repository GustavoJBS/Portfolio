<script lang="ts">
    import { defineComponent } from 'vue'
    import Uninter from '@/assets/img/schools/uninter.png'
    import Clovis from '@/assets/img/schools/clovis.png'
    import Etec from '@/assets/img/schools/etec.png'

    export default defineComponent({
        data() {
            return {
                educationHistory: [
                    {
                        course: 'Systems Analysis and Development',
                        school: 'Uninter', 
                        dateRange: 'March 2021 - May 2023',
                        logo: Uninter
                    },
                    {
                        course: 'Computer Technician',
                        school: 'Clóvis Bevilacqua College ', 
                        dateRange: 'November 2021 - April 2022',
                        logo: Clovis
                    },
                    {
                        course: 'Industrial Automation Technician',
                        school: 'Etec São Paulo', 
                        dateRange: 'February 2021 - March 2022',
                        logo: Etec
                    },
                ]
            }
        },
    })
</script>

<template>
    <div class="flex w-full py-8 flex-col items-center" id="education">
        <div class="m-auto w-full lg:max-w-4xl text-center flex flex-col gap-2 justify-center items-center text-athens-gray-100">
            
            <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-l from-fuchsia-500 via-red-600 to-orange-400">
                Education Experience
            </h1> 

            <div class="flex w-full flex-col divide-y divide-athens-gray-300">
                <div 
                    v-for="course in educationHistory" 
                    class="flex w-full divide-y-2 divide-athens-gray-300 flex-col"
                >
                    <div class="flex flex-col lg:flex-row py-8 w-full justify-between items-center">
    
                        <img 
                            class="h-36 max-w-[14rem] mb-4 object-contain" 
                            v-if="course.logo"
                            :src="course.logo" 
                            :alt="`${course.school} Company Logo`" 
                        />
    
                        <div class="flex flex-col w-full h-full text-start lg:text-end lg:justify-between">
                            <div class="flex flex-col gap-1">
                                <h1 class="text-2xl font-bold text-cod-gray-900">
                                    {{ course.school }}
                                </h1>
                                <h2 class="text-xl text-cod-gray-800 font-semibold">
                                    {{ course.course }}
                                </h2>
                            </div>
    
                            <h2 class="text-xl text-cod-gray-800 font-semibold">
                                {{ course.dateRange }}
                            </h2>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>