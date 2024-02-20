<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Ayurveda, the oldest recorded healing science, focuses on longevity, contentment, and well-balanced life. It acknowledges individuality and uses a holistic approach to assess health conditions, harmonising physical and mental balance.",
                " It uses natural interventions to prevent, heal, and manage acute and chronic health conditions without side effects. Common conditions include insomnia, skin conditions, stress, headaches, migraines, weight management, autoimmune disease, respiratory conditions, compromised immune systems, arthritis, and gastro-intestinal problems.",
                "Ayurveda aims to prevent and alleviate diseases, promoting health and happiness for individuals and society. "
            ],
            description:
                "",
                imgUrl: "assets/realayurveda.png",
        },
        {
            featureList: [
                "Holistic medicine, based on tradition, emphasizes the importance of food as a first medicine and the kitchen as a pharmacy. Ayurvedic medicine focuses on the body's natural strength, allowing it to heal naturally. Herbal medicine supplements treat symptoms and aids in unwinding disease processes, freeing the body from the root cause of aggravating symptoms. Foods and spices are recommended for therapeutic use, providing subtle nutrition and stimulating deeper tissues and organs.",
            ],
            description:
                "",
                imgUrl: "assets/herbs.png",
        },
        {
            featureList: [
                "Lifestyle disorders can be caused by unhealthy habits, inactivity, and a disturbed biological clock. Ayurveda emphasizes health as a radiant state of vigor and energy achieved through balance in daily activities. Seasonal and weather changes significantly impact the body, so adaptations to diet and lifestyle are crucial. Epigenetics supports this Ayurvedic principle.",
            ],
            description:
                "",
                imgUrl: "assets/lifestyle.png",
        },{
            featureList: [
                "Lifestyle disorders can be caused by unhealthy habits, inactivity, and a disturbed biological clock. Ayurveda emphasizes health as a radiant state of vigor and energy achieved through balance in daily activities. Seasonal and weather changes significantly impact the body, so adaptations to diet and lifestyle are crucial. Epigenetics supports this Ayurvedic principle. "
            ],
            description:
                "",
                imgUrl: "assets/realmeditate.png",
        },{
            featureList: [
                "Ayurveda, the oldest recorded healing science, focuses on longevity, contentment, and well-balanced life. It acknowledges individuality and uses a holistic approach to assess health conditions, harmonising physical and mental balance.",
                " It uses natural interventions to prevent, heal, and manage acute and chronic health conditions without side effects. Common conditions include insomnia, skin conditions, stress, headaches, migraines, weight management, autoimmune disease, respiratory conditions, compromised immune systems, arthritis, and gastro-intestinal problems.",
                "Ayurveda aims to prevent and alleviate diseases, promoting health and happiness for individuals and society. "
            ],
            description:
                "",
                imgUrl: "assets/realmeditate.png", /* place holder */
        },
    ];
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Start your spiritual & holistic <span class="text-green-400"
                    >retreat</span
                > today
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Features For Everyone
            </h3>
        </div>

        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    What is  <span
                        class="text-green-400 font-medium">Ayurveda</span
                    >?
                {:else if index === 1}
                    Herbs and Home Remedies
                {:else if index === 2}
                    Lifestyle and Daily <span
                        class="text-green-400 font-medium">Routines</span>
                {:else if index === 3}
                    Yoga &  <span
                        class="text-green-400 font-medium">Breathing</span>
                        Techniques
                {:else if index === 4}
                    Integrative <span
                        class="text-green-400 font-medium">Vedic</span>
                        Counseling
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>
