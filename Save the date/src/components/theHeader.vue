<template>
    <div class="header">
        <div class="monogram">Carolina e Wanderson</div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Presents List</a></li>
                <li><a href="#">Location Address</a></li>
            </ul>
        </nav>
    </div>

</template>
<script setup>
</script>
<style>
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: #f8f9fa;
    border-bottom: 1px solid #e9ecef;
}

.monogram {
    font-size: 2rem;
    font-weight: bold;
}

nav ul {
    gap: 1rem;
    display: flex;
    list-style: none;
}
</style>