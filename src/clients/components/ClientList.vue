<script setup lang="ts">
import type { Client } from '@/clients/interfaces/client'

interface Props {
    clients: Client[]
}

const props = defineProps<Props>()
 

</script>

<template>
    <!-- <span>{{ props }}</span> -->
    <ul>
        <li v-for="client of clients" :key="client.id">
            <RouterLink :to="{
                name: 'client-id',
                params: { id: client.id },
            }"> {{  client.name }}
            </RouterLink>
        </li>
    </ul>
</template>


<style scoped>

</style>