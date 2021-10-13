<template>

    <div>

        <div class="flex justify-between mt-8 items-center" :class="{ 'mb-4': $scopedSlots.default }">

            <h4>{{ title }}</h4>

            <slot name="filters"></slot>

        </div>

        <div class="flex flex-wrap mt-6" v-if="$scopedSlots.default">

            <slot/>

        </div>

    </div>

</template>

<script>

    export default {
        props: {
            title: {
                type: String,
                required: true
            }
        }
    }

</script>
