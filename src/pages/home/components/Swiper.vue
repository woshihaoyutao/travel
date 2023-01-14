<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" /></swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>
<script>
export default {
    name: "HomeSwiper",
    data() {
        return {
            swiperOption: {
                pagination: ".swiper-pagination",
                loop: true
            },
            swiperList: [
                {
                    id: "0001",
                    imgUrl: "https://www.niuqiqi.com/uploadfile/202112/d114cc19ac1852.jpg"
                },
                {
                    id: "0002",
                    imgUrl:
                        "https://www.niuqiqi.com/uploadfile/202112/6d42c79e1d7f15b.jpg"
                }
            ]
        };
    }
};
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background:#fff
.wrapper
    overflow: hidden
    width: 100% 
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
        width: 100%
</style>
