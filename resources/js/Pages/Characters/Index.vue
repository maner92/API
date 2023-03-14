<template>
    <AppLayout>
        <div class="container">
            <div class="row align-items-center justify-content-center">
                <div v-for="character in characters.data" :key="character">
                    <div v-if="character.isPlayableCharacter == true
                    ">
                        <div class="card mb-3" style="max-width: 540px;">
                            <div class="row g-0">
                                <div class="col-md-4">
                                    <img :src=character.fullPortrait class="img-fluid rounded-start" alt="">
                                </div>
                                <div class="col-md-8">
                                    <div class="card-body">
                                        <h1 class="card-title">{{ character.displayName }}</h1>
                                        <p class="card-text">{{ character.description }}</p>
                                        <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                                            <button type="button" class="btn btn-outline-danger">See info</button>
                                        </div>
                                    </div>
                                </div>

                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AppLayout>
</template>

<script>
import AppLayout from '@/Layouts/AppLayout.vue';
export default {
    props: {
        characters: Object
    },
    components: {
        AppLayout
    }
}
</script>

<style></style>