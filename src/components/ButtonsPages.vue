<template>
    <div>
        <div>
            <a :class="button.class" href="#">{{button.number}}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ButtonsPages',
    props: {
        button: {
            type: Object,
            required: true
        }
    },
    data() {
        return {

        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>