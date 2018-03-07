<template>
<!-- 使用轮播组件：npm install vue-awesome-swiper -->
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{ name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <!-- 指示器 -->
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
        </swiper>
    </section>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"

export default {
    props: {
        cname: {
            type: String,
            default: ""
        },
        options: {
            type: Object,
            default() {
                return {
                    autoplay: true,
                    loop: true,
                    pagination: {
                        el: ".swiper-pagination"
                    },
                    notNextTick: false
                }
            }
        },
        items: {
            type: Array,
            default() {
                return []
            }
        }
    },
    components: {
        swiper,
        swiperSlide
    }
}
</script>

<style lang="css">
  @import "~swiper/dist/css/swiper.css";
</style>