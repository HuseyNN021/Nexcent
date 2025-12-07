<script setup>
import unlockImg from '../assets/UnlockImg.webp'
import Button from './Button.vue'
import PageSection from './PageSection.vue'
const title=' The unseen of spending three years at Pixelgrade'
const description='Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet justo ipsum. Sed accumsan quam vitae est varius fringilla. Pellentesque placerat vestibulum lorem sed porta. Nullam mattis tristique iaculis.   Nullam pulvinar sit amet risus pretium auctor. Etiam quis massa pulvinar, aliquam quam vitae, tempus sem.   Donec elementum pulvinar odio.'
console.log(typeof(unlockImg));

</script>

<template>
    <PageSection :img="unlockImg" :title="title" :description="description"/>
</template>