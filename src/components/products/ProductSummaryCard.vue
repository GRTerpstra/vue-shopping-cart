<template>
    <div class="card">
        <h3> {{product.name}} </h3>

        <h5 class="price">Price: ${{product.price.toFixed(2)}}</h5>
        <p class="description">Description: {{ description }}</p>
        <p class="text-muted">{{ product.category }}</p>
        <button class="view-product-button" @click="$emit('view-product', product)" >View Product</button>
    </div>
</template>

<script>
import './ProductSummaryCard.scss'

    export default {
        props: ['product'],
        computed: {
            description() {
                return this.product.description.substring(0, 150)
            }
        }
    }
</script>

