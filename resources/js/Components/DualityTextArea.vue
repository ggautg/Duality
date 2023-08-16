<script setup>
import { onMounted, ref } from "vue";

defineProps({
    modelValue: String,
    label: String,
})

defineEmits(['update:modelValue'])

const input = ref(null)

onMounted(() => {
    if (input.value.hasAttribute('autofocus')) {
        input.value.focus();
    }
});

defineExpose({ focus: () => input.value.focus() });
</script>

<template>
    <div class="relative z-0">
        <textarea rows="6"
            class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-200 appearance-none  focus:outline-none focus:ring-0 focus:border-gray-200 peer"
            placeholder=" " ref="input" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)">
        </textarea>
        <label
            class="absolute text-duality duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-duality peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6
    peer-hover::left-0 peer-hover:text-duality peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-hover:scale-75 peer-hover:-translate-y-6">{{
        label }}</label>
    </div>
</template>

