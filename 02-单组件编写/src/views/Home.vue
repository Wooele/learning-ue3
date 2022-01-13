<template>
    <h1>Hello World</h1>
</template>

<script lang="ts">
import { onBeforeMount, reactive, toRefs, onMounted} from 'vue'

export default {
    setup () {
        console.log('--setup start--');
        const state = reactive({
            count: 0,
        });
        onBeforeMount(() => {
            console.log('--onBeforeMount')
        });
        onMounted(() => {
            console.log('--onMounted')
        });
        console.log('--setup end--');
        return {
            ...toRefs(state),
        }
    }
}
</script>

<style scoped>

</style>