<template>
    <h1>Calendar Page</h1>
    <p>This is the calendar page</p>
    <ClientOnly>
        <DatePicker v-model="date"/>
    </ClientOnly>

</template>
<script setup>
    const DatePicker = defineAsyncComponent(async () => {
        const { DatePicker } = await import('v-calendar');
        import ('v-calendar/style.css');
        return DatePicker;
    });
        
    const date = ref(new Date());
</script>