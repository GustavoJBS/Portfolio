<script setup lang="ts">
    import Education from '@/components/home/Education.vue';
    import Introduction from '@/components/home/Introduction.vue';
    // import Projects from '@/components/home/Projects.vue';
    import Works from '@/components/home/Works.vue';
</script>

<template>
    <main class="p-8 divide-y-2 divide-athens-gray-300">
        <Introduction />

        <Works />

        <Education />

        <!-- <Projects /> -->
    </main>
</template>
