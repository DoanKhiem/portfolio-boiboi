<template>
    <div class="mx-auto py-5 px-4">
        <div class="bg-primary border-4 rounded-[40px] border-[#d7a947] text-white">
            <h2 class="abril-fatface-regular-font text-5xl md:text-6xl uppercase text-center mt-5">My Resume</h2>
            <div class="relative z-20 mt-5">
                <h3 class="bg-[#d7a947] rounded-[40px] inline-block px-5 py-1 text-xl md:text-2xl">Me Through Numbers</h3>
                <div class="bg-[#d7a947] h-1 w-full absolute top-1/2 left-1 -z-10"></div>
            </div>
            <div class="grid md:grid-cols-5 p-4">
                <div class="md:col-span-2">
                    <img src="~/assets/images/avt-2.png" alt="Image Avatar"
                        class="w-full object-cover mb-4 transition-transform duration-300 hover:scale-105">
                </div>
                <div class="md:col-span-3">
                    <div class="grid grid-cols-2 gap-4 md:gap-8 md:px-10 mt-5">
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>5</p>
                            <p>Projects</p>
                        </div>
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>8.9</p>
                            <p>GPA</p>
                        </div>
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>4</p>
                            <p>Events</p>
                        </div>
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>10,000</p>
                            <p>Supporters</p>
                        </div>
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>15,400,00</p>
                            <p>Money Rasing</p>
                        </div>
                        <div class="text-center text-3xl md:text-5xl bg-[#954b58] py-5">
                            <p>150</p>
                            <p>Members</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <Education />
        <Awards />
        <Experiences />
        <WorkExperience />
    </div>
    
</template>

<script setup lang="ts">

</script>

<style scoped></style>