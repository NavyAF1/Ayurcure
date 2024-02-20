<script>
    import CtAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
</script>

<SectionWrapper>
    <Header />
    <div
        class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <h2
            class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold">
            <img src="assets/realbg.png" alt="assets/realbg.png" width="400px" height="50px" class="image">
            <span class="text-green-400">Ancient</span> Wisdom
            <span>For Modern  <span class="text-green-400">Times</span></span>
        </h2>
        <p
            class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
        >
        AyuCure Wellness offers complimentary and alternative medicine with a natural and holistic approach to promote healing and wellness. 
        Its adherents strive to create harmony between the body, mind, and spirit. 
        Maintaining this balance prevents illness, heal acute conditions, and contributes to a long and healthy life. <span class="italic">
            </span>
        </p>
        <CtAs />
       <Stars/>
    </div>
</SectionWrapper>