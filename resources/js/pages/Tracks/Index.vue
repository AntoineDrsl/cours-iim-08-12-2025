<template>
    <MusicLayout>
        <template #title>
            Liste des musiques
        </template>

        <template #actions>

        </template>

        <template #content>
            <div class="grid grid-cols-4 gap-4">
                <Track
                    v-for="track in tracks"
                    :key="track.slug"
                    :track="track"
                />
            </div>
        </template>
    </MusicLayout>
</template>

<script>
    import MusicLayout from '@/layouts/MusicLayout.vue';
    import Track from '@/components/Tracks/Track.vue';

    export default {
        name: 'Index',
        components: {
            MusicLayout,
            Track,
        },
        props: {
            tracks: Array,
        }
    }
</script>
