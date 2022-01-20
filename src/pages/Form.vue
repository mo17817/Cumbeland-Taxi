<template>
    <div class = "col-5 bg-primary">
        <Form></Form>
        </div>
</template>
<script>
import { defineComponent } from '@vue/composition-api';
import components from 'vue'
import { Form } from "components/Form.vue";

export default defineComponent({
    setup() {
    },components: { Form },
})
</script>
