<template>
    <div class="container my-5">
        <div style="max-width:600px;width:100%">
            <div class="d-flex align-items-center gap-3">
                <div style="width:0.6rem;height:0.6rem" class="rounded-circle bg-dark"></div>
                <span>Blog and articles</span>
            </div>
            <h1 class="display-4 mt-2">Latest insights and trends</h1>
        </div>
        <div class="row mt-md-5 mt-2 g-4">
            <div v-for="list in news_list" class="col-xl-4 col-md-6">
                <div class="px-3 px-md-0 mb-4 mb-md-0">
                    <div class="w-100 h-auto bg-body-secondary rounded-4" style="aspect-ratio: 1;">
                        <img loading="lazy" class="w-100 h-auto bg-body-secondary rounded-4" style="aspect-ratio: 1;object-fit: cover;" :src="list.img" v-if="list.img" alt=""/>
                    </div>
                    <div class="px-2 d-flex flex-column gap-3 mt-4">
                        <div>
                            <span class="bg-body-secondary p-2">
                                News
                            </span>
                        </div>
                        <h6 class="m-0 h4" style="font-weight: 400;">{{ list?.title || "Unknown news title" }}</h6>
                        <p class="m-0 text-secondary">{{ list?.content || "Unknown news content" }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const news_list = [
        {
            img:"/img/news-1.jpg",
            title:"The Ultimate Guide to Budgeting in 2024",
            content:"Master the art of budgeting with our comprehensive guide. Learn how to create a budget that works for you."
        },
        {
            img:"/img/news-2.jpg",
            title:"The Ultimate Guide to Budgeting in 2024",
            content:"Master the art of budgeting with our comprehensive guide. Learn how to create a budget that works for you."
        },
        {
            img:"/img/news-3.jpg",
            title:"The Ultimate Guide to Budgeting in 2024",
            content:"Master the art of budgeting with our comprehensive guide. Learn how to create a budget that works for you."
        }
    ]
</script>