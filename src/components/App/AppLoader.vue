<template>
    <div class="app-loader">
        <div class="preloader-wrapper big active">
            <div class="spinner-layer spinner-blue-only">
                <div class="circle-clipper left">
                    <div class="circle"></div>
                </div>
                <div class="gap-patch">
                    <div class="circle"></div>
                </div>
                <div class="circle-clipper right">
                    <div class="circle"></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import {computed} from 'vue'

    export default {
        setup() {
            const color = computed(() => {
                const colors = ['spinner-blue-only', 'spinner-red-only', 'spinner-green-only']
                return colors[Math.floor(Math.random() * 3)]
            })

            return {
                color
            }
        }
    }

</script>

<style scoped>

</style>