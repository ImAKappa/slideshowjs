<script lang="ts">
    import IntersectionObserver from 'svelte-intersection-observer';

    // export let visible = false;
    export let threshold = 1.0;

    let node;
</script>

<IntersectionObserver element={node} let:intersecting {threshold}>
    <div bind:this={node}>
        <div class="text-container" style="opacity: {intersecting ? '1.0' : '0.0'};">
            <slot />
        </div>
    </div>
</IntersectionObserver>

<style>
    .text-container {
        transition-duration: 3s;
    }
</style>