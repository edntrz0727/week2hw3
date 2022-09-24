<template>
    <h1>
        This is HomeWork 3
    </h1>
    <br/>
    <h1>
        Templating
    </h1>
    <div>
        <Password v-model="value4">
            <template #header>
                <h6>Pick a password</h6>
            </template>
            <template #footer="sp">
                {{sp.level}}
                <Divider />
                <p class="mt-2">Suggestions</p>
                <ul class="pl-2 ml-2 mt-0" style="line-height: 1.5">
                    <li>At least one lowercase</li>
                    <li>At least one uppercase</li>
                    <li>At least one numeric</li>
                    <li>Minimum 8 characters</li>
                </ul>
            </template>
        </Password>
    </div>
</template>
<script setup lang="ts">
    import { ref } from 'vue';
    const value4 = ref();
</script>