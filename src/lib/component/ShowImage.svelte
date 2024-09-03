<script>
    import zharan from '$lib/images/handicrafts/zharan.png';
    import bamboo_weave from '$lib/images/handicrafts/bamboo_weave.png';
    import Dali_wood_carving from '$lib/images/handicrafts/Dali_wood_carving.png';
    import jianchuan_black_pottery from '$lib/images/handicrafts/jianchuan_black_pottery.png';
    import Miao_reed_pipe from '$lib/images/handicrafts/Miao_reed_pipe.png';
    import tile_cats from '$lib/images/handicrafts/tile_cats.png';


    let images = [
        {
            src: zharan,
            description: 'Bai tie-dye'
        },
        {
            src: bamboo_weave,
            description: 'bamboo_weave'
        },
        {
            src: Dali_wood_carving,
            description: 'Dali_wood_carving'
        },
        {
            src: jianchuan_black_pottery,
            description: 'jianchuan_black_pottery'
        },
        {
            src: Miao_reed_pipe,
            description: 'Miao_reed_pipe'
        },
        {
            src: tile_cats,
            description: 'tile_cats'
        }
    ];
</script>

<style>
    .gallery {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 20px;
    }

    .item {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
    }

    .item img {
        margin-right: 20px;
        border: 1px solid #ccc;
        width: 600px;
        height: 400px;
    }

    .description {
        max-width: 300px;
    }
</style>

<div class="gallery">
    {#each images as { src, description }}
        <div class="item">
            <!-- svelte-ignore a11y-img-redundant-alt -->
            <img src={src} alt={description}>
            <div class="description">{description}</div>
        </div>
    {/each}
</div>
