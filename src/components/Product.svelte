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
                "Swoley moley ensures all users have the information they need to train safely and train effectively. Ayurveda empowers individuals to take control of their health.",
                imgUrl: "assets/realayurveda.png",
        },
        {
            featureList: [
                "Select your preferences",
                "Personalize your workouts",
                "Customize your training",
                "Guarantees progress on all core exercises",
            ],
            description:
                "Build you streaks and see your progress with our amazing tracking and analytics features.",
                imgUrl: "assets/herbs.png",
        },
        {
            featureList: [
                "Eliminating guesswork",
                "Save time",
                "Achieve the performance you seek",
                "Builds functional strength",
            ],
            description:
                "Enter as much information about yourself as you desire to ensure all workouts are personalized to your every need.",
                imgUrl: "assets/lifestyle.png",
        },{
            featureList: [
                "Ayurveda, the oldest recorded healing science, focuses on longevity, contentment, and well-balanced life. It acknowledges individuality and uses a holistic approach to assess health conditions, harmonising physical and mental balance.",
                " It uses natural interventions to prevent, heal, and manage acute and chronic health conditions without side effects. Common conditions include insomnia, skin conditions, stress, headaches, migraines, weight management, autoimmune disease, respiratory conditions, compromised immune systems, arthritis, and gastro-intestinal problems.",
                "Ayurveda aims to prevent and alleviate diseases, promoting health and happiness for individuals and society. "
            ],
            description:
                "Swoley moley ensures all users have the information they need to train safely and train effectively. Ayurveda empowers individuals to take control of their health.",
                imgUrl: "assets/realmeditate.png",
        },{
            featureList: [
                "Ayurveda, the oldest recorded healing science, focuses on longevity, contentment, and well-balanced life. It acknowledges individuality and uses a holistic approach to assess health conditions, harmonising physical and mental balance.",
                " It uses natural interventions to prevent, heal, and manage acute and chronic health conditions without side effects. Common conditions include insomnia, skin conditions, stress, headaches, migraines, weight management, autoimmune disease, respiratory conditions, compromised immune systems, arthritis, and gastro-intestinal problems.",
                "Ayurveda aims to prevent and alleviate diseases, promoting health and happiness for individuals and society. "
            ],
            description:
                "Swoley moley ensures all users have the information they need to train safely and train effectively. Ayurveda empowers individuals to take control of their health.",
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