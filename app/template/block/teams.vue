<template>
    <div class="container my-5" data-aos="fade">
        <div style="max-width:600px;width:100%">
            <div class="d-flex align-items-center gap-3">
                <div style="width:0.6rem;height:0.6rem" class="rounded-circle bg-dark"></div>
                <span>Expertise</span>
            </div>
            <h1 class="display-4 mt-2">Meet the Financer team</h1>
            <p class="text-secondary mt-4">Meet the talanted individuals who drive our company's success with their dedication, expertise, and passion for innovation</p>
        </div>
        <div class="w-100  mt-5">
            <div class="row g-4 px-4 px-sm-0">
                <div v-for="(list,index) in teams_list" data-aos="fade-up" :data-aos-delay="index*150" class="col-xl-4 col-md-6">
                    <div class="w-100 h-auto bg-body-secondary rounded-4 position-relative" style="aspect-ratio: 1;">
                        <img 
                            v-if="list.id" 
                            :src="`/img/team/${list.id}-516.webp`"
                            :srcset="`
                                /img/team/${list.id}-304.webp 304w,
                                /img/team/${list.id}-400.webp 400w,
                                /img/team/${list.id}-516.webp 516w
                            `"
                            :title="list?.author || `Unknown`" 
                            class="w-100 h-auto bg-body-secondary rounded-4" 
                            style="aspect-ratio: 1;object-fit: cover;" 
                            loading="lazy"
                            alt=""
                        />
                        <div class="position-absolute w-100 p-4" style="bottom:0">
                            <div class="w-100 bg-body p-3 rounded-4 d-flex flex-wrap gap-2 align-items-center">
                                <div class="flex-fill">
                                    <h1 class="h4 m-0" style="font-weight: 400;">{{ list?.name || "Unknown" }}</h1>
                                    <p class="m-0 text-secondary mt-2">{{ list?.desc || "Unknown job desc" }}</p>
                                </div>
                                <div class="border rounded-circle" style="width: clamp(20px, 8vw, 60px);aspect-ratio: 1 / 1;flex-shrink: 0;">
                                    <button class="btn p-1 rounded-circle d-flex align-items-center justify-content-center w-100 h-100">
                                        <svg width="36" height="36" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <path d="M17.303 2.25H6.69698C5.51757 2.25 4.38647 2.71852 3.5525 3.55249C2.71853 4.38646 2.25 5.51757 2.25 6.69698V17.303C2.25 18.4824 2.71853 19.6135 3.5525 20.4475C4.38647 21.2815 5.51757 21.75 6.69698 21.75H17.303C18.4824 21.75 19.6136 21.2815 20.4475 20.4475C21.2815 19.6135 21.75 18.4824 21.75 17.303V6.69698C21.75 5.51757 21.2815 4.38646 20.4475 3.55249C19.6136 2.71852 18.4824 2.25 17.303 2.25ZM8.84265 17.9923C8.84568 18.0467 8.83757 18.1011 8.81882 18.1523C8.80007 18.2035 8.77106 18.2502 8.73359 18.2898C8.69612 18.3293 8.65097 18.3608 8.6009 18.3823C8.55084 18.4038 8.49691 18.4149 8.44243 18.4148H6.66363C6.55647 18.4119 6.45468 18.3673 6.37992 18.2904C6.30517 18.2136 6.26336 18.1106 6.2634 18.0034V10.5992C6.26191 10.5457 6.27118 10.4925 6.29063 10.4426C6.31007 10.3928 6.3393 10.3473 6.37662 10.309C6.41393 10.2706 6.45857 10.2402 6.50787 10.2193C6.55716 10.1985 6.61012 10.1878 6.66363 10.1879H8.44243C8.49593 10.1878 8.54889 10.1985 8.59819 10.2193C8.64749 10.2402 8.69212 10.2706 8.72944 10.309C8.76675 10.3473 8.796 10.3928 8.81544 10.4426C8.83489 10.4925 8.84414 10.5457 8.84265 10.5992V17.9923ZM7.51968 8.63141C7.22991 8.62922 6.94729 8.54129 6.70743 8.37871C6.46757 8.21613 6.2812 7.98618 6.17183 7.71784C6.06246 7.4495 6.03499 7.15479 6.09286 6.87086C6.15073 6.58693 6.29137 6.32649 6.49704 6.12236C6.70271 5.91824 6.9642 5.77957 7.24856 5.72385C7.53292 5.66812 7.82742 5.69782 8.09492 5.80921C8.36242 5.9206 8.59096 6.10869 8.75173 6.34978C8.91249 6.59086 8.99829 6.87414 8.9983 7.16391C8.9983 7.35757 8.95998 7.54931 8.88554 7.72808C8.8111 7.90685 8.702 8.06913 8.56455 8.20554C8.4271 8.34196 8.26401 8.44982 8.08467 8.52291C7.90534 8.59601 7.71332 8.63288 7.51968 8.63141ZM18.3369 17.9812C18.337 18.0825 18.2975 18.1798 18.2269 18.2525C18.1564 18.3251 18.0602 18.3674 17.959 18.3703H16.0801C15.9788 18.3674 15.8827 18.3251 15.8121 18.2525C15.7415 18.1798 15.7021 18.0825 15.7021 17.9812V14.557C15.7021 14.0456 15.8578 12.3335 14.3458 12.3335C13.1673 12.3335 12.9339 13.5342 12.8894 14.0678V18.059C12.8894 18.1603 12.85 18.2576 12.7794 18.3303C12.7088 18.403 12.6127 18.4452 12.5114 18.4481H10.6882C10.6371 18.4481 10.5865 18.4381 10.5392 18.4185C10.492 18.3989 10.4491 18.3703 10.413 18.3342C10.3769 18.298 10.3482 18.2551 10.3287 18.2079C10.3091 18.1607 10.299 18.1101 10.299 18.059V10.5658C10.3019 10.4646 10.3442 10.3685 10.4169 10.2979C10.4895 10.2273 10.5869 10.1878 10.6882 10.1879H12.5114C12.6127 10.1878 12.71 10.2273 12.7827 10.2979C12.8554 10.3685 12.8976 10.4646 12.9005 10.5658V11.2107C13.1667 10.8212 13.5341 10.5119 13.9632 10.316C14.3922 10.12 14.8666 10.045 15.3352 10.0989C18.3703 10.0989 18.3592 12.9339 18.3592 14.5459L18.3369 17.9812Z" fill="currentColor"/>
                                        </svg>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const teams_list = [
        {
            id:"team-6",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Фотограф: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719797/"
        },
        {
            id:"team-1",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Фотограф: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719795/"
        },
        {
            id:"team-2",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Автор фото с Pexels: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719793/"
        },
        {
            id:"team-3",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Фотограф: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719797/"
        },
        {
            id:"team-4",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Фотограф: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719797/"
        },
        {
            id:"team-5",
            name:"Marcus Mango",
            desc:"Head of Marteking",
            author:"Фотограф: SAULO LEITE: https://www.pexels.com/ru-ru/photo/19719797/"
        }
    ]
</script>