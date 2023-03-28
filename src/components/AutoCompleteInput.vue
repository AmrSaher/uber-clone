<template>
    <div id="AutoCompleteInput" class="flex items-center">
        <input 
            :id="theId" 
            v-model="inputComputed" 
            @click="emit('isActive', true)" 
            type="text" 
            class="text-md bg-gray-100 appearance-none
            w-full py-2.5 px-3 text-gray-700
            leading-tight focus:outline-none
            focus:shadow-outline
            focus:bg-gray-200"
            :placeholder="placeholder"
            autocomplete="off"
        />
        <WindowCloseIcon @click="emit('clearInput')" fillColor="#2e2e2b" />
    </div>
</template>

<script setup>
import { toRefs, defineProps, defineEmits, computed } from 'vue'

import WindowCloseIcon from 'vue-material-design-icons/WindowClose.vue'

const emit = defineEmits(['update:input', 'clearInput', 'isActive'])

const props = defineProps({
    theId: String,
    input: String,
    placeholder: String
})

const { theId, input, placeholder } = toRefs(props)

const inputComputed = computed({
    get: () => input.value,
    set: (val) => emit('update:input', val)
})
</script>