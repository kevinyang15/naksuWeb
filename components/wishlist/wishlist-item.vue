<template>
    <tr>
        <td class="tp-cart-img">
            <nuxt-link :href="`/shop-details/${item.id}`">
                <img :src="item.img" :alt="item.title" />
            </nuxt-link>
        </td>

        <td class="tp-cart-title">
            <nuxt-link :href="`/shop-details/${item.id}`">{{ item.title }}</nuxt-link>
        </td>

        <td class="tp-cart-price"><span>{{ formatPrice(item.price, true) }}</span></td>

        <td class="tp-cart-add-to-cart">
            <button type="submit" class="tp-btn">Add To Cart</button>
        </td>

        <td class="tp-cart-action">
            <button class="tp-cart-action-btn">
                <svg-close clr="currentColor" />
                <span>Remove</span>
            </button>
        </td>
    </tr>
</template>

<script setup lang="ts">
import { formatPrice } from "@/lib/format-price";
import type { ICart } from "@/types/cart-type";

// Props
defineProps<{ item: ICart; }>();
</script>