<template>
    <div>
        <div v-for="customersData in customers" :key="customersData.id">
            <p>We have {{ customersData.name }} from {{ customersData.address }}.</p>
        </div>
    </div>
</template>

<script setup>
    // import Customers from '@/Pages/Customers/Create.vue';
    defineProps(['customers']);
</script>

