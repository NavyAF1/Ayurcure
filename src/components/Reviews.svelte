<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";

    let lim = true;

    let reviewsList = [
        {
            name: "Bhanu Mehta",
            review: "I cannot express my satisfaction with the services me and my wife got from Ayucure. She was courteous, professional, and made our visits as comfortable as she possibly could. It was good to be treated with such professionalism and care. I am truly grateful. I appreciated all her follow-ups and her willingness to answer any questions. A big thank you to Vaidya Preeti Patel !!! ",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: "Indiana Leal",
            review: "Both my mom and myself have had amazing results with her care, and recommendations. She is always available, and willing to help. A great professional truly dedicated to her patients, and making sure that her patients regain their health. Highly recommended.",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: "Corina Clemente",
            review: "I love Vaidhya Preeti! She is amazing! So compassionate, and really understands health in holistic way. Also, she is really good at motivating clients to actually make changes in their lifestyles. My whole family does skype consults with here from Panama, and her loving approach has made a huge difference in our lives. Highly recommended!",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: "Meredith Shaw",
            review: "Vaidhya Preeti is kind and caring. Her recommendations are always comprehensive. I have had great results from her services for myself and my two children. I recommend her to friends and family all the time.",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: " Aishwarya Dev Pendyala",
            review: "The most competent and vibrant Ayurveda Vaidhya I have ever come across. She treats all her patients with so much care, taking note of the finest of details! I have recommended her to all of my inner circle and I just won’t stop there! Gold mine and definitely my vaidhya forever!",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: "Jonathan Sandler",
            review: "We love AYUCURE!! me and my wife have went to different natural doctors and traditional doctors but without much success. Now we are following Preeti's guidelines and our health has been improved over 90% in just a couple of weeks. My wife has been suffering from gastritis and body pain and I had overweight and thyroid problems. Also anxiety and mind stress have released a lot with just a couple of changes in our diet and teas suggested by Preeti. I really recommend her.",
            features: [
                "",
                "",
                "",
            ],
        },
        {
            name: "Marinell Correa",
            review: "Vaidhya Preeti is a very friendly and patient person who has given me a lot of good advises as an Ayurveda Doctor. For sure she will succeed in her practice because she is very dedicate to people’s well being.",
            features: [
                "",
                "",
                "",
            ],
        },  
        {
            name: " Hardeep Bansal",
            review: "Vaidhya Preeti is awesome Ayurveda practitioner. She is the most caring, nicest herbalist I have ever met. I can't go to Edmonton all the time because I live in Calgary but she always takes time to answer my questions. Very concerned about my problems. I wish others can experience her care and expertise as a doctor.",
            features: [
                "",
                "",
                "",
            ],
        },
    ];
</script>

<SectionWrapper id="reviews">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Don't just take our word for it
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                See What <span class="text-green-400">Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
        <div class="flex flex-col gap-10">
            <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                Trusted by over 1,000 clients
            </p>
            <Stars />
        </div>
    </div>
</SectionWrapper>