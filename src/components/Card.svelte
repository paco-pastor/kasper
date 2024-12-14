<script>
    export let title = "Card Title";
    export let imageUrl = "https://via.placeholder.com/150";
</script>

<div class="card">
    <p class="card-title">{title}</p>
    <img class="card-image" src={imageUrl} alt={title} />
</div>

<style>
    .card {
        border: 1px solid #f327af;
        border-radius: 8px;
        padding: 16px;
        box-shadow: 0 2px 4px rgba(243, 39, 175, 0.5);
        max-width: 300px;
        margin: 16px;
        background-color: #040103;
        color: #f327af;
    }
    .card-title {
        font-family: kasper;
        font-size: 1.25em;
        margin-bottom: 8px;
        color: #f327af;
    }
    .card-image {
        max-width: 100%;
        border-radius: 8px;
    }
</style>