<template>
    <div class="container-fluid bg-body-secondary mt-5 py-5">
        <div class="container">
            <div style="max-width:600px;width:100%">
                <div class="d-flex align-items-center gap-3">
                    <div style="width:0.6rem;height:0.6rem" class="rounded-circle bg-dark"></div>
                    <span>Testimonials</span>
                </div>
            </div>
            <div class="row mt-1 g-5">
                <div v-for="list in reviews_list" class="col-lg-4 col-md-6">
                    <h1 class="h4" style="font-weight: 400;">"Advisory has been a game-changer for our businesses. With its comprehesive financial management tools, we've been able to streamline our processes and make more informed decisions. The customer support team is also top-notch"</h1>
                    <div class="d-flex gap-4 mt-4">
                        <div style="width:60px;height:60px;" class="rounded-circle bg-body-tertiary">
                            <img loading="lazy" style="width:60px;height:60px;" class="rounded-circle bg-body-tertiary" v-if="list.img" :src="list.img" alt=""/>
                        </div>
                        <div class="flex-fill d-flex flex-column justify-content-center gap-1">
                            <h5 class="m-0">{{ list?.name || "Unknown" }}</h5>
                            <p class="m-0 text-secondary">{{ list?.desc || "Unknown" }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
    const reviews_list = [
        {
            img:"/img/review-1.jpg",
            name:"John Doe",
            desc:"CEO, Tech Innovations"
        },
        {
            img:"/img/review-2.jpg",
            name:"John Doe",
            desc:"CEO, Tech Innovations"
        },
        {
            img:"/img/review-3.jpg",
            name:"John Doe",
            desc:"CEO, Tech Innovations"
        },
    ]
</script>