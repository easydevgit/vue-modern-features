<script setup lang="ts">
const slots = defineSlots<{
    title?: (props: { msg?: string }) => any
    body?: (props: { short: boolean }) => any
    default?: (props: {}) => any;
}>()
</script>

<template>
    <dialog id="my_modal_1" class="modal" open>
        <div class="modal-box">
            <h3 class="font-bold text-lg">
                <slot name="title" />
                <p v-if="!slots.title">Some title</p>
            </h3>
            <slot name="body" :short="false" />
            <slot></slot>
            <div class="modal-action">
                <form method="dialog">
                    <!-- if there is a button in form, it will close the modal -->
                    <button class="btn">Close</button>
                </form>
            </div>
        </div>
    </dialog>
</template>