<template>
    <div class=" mx-auto py-5 px-4">
        <div class=" text-white">
            <h2 class=" abril-fatface-regular-font text-5xl md:text-6xl uppercase text-primary text-center mb-5">HEALING
                BOXES</h2>

            <div class="grid grid-cols-2 md:grid-cols-3 gap-5">
                <div v-for="item in arrayBoxs" :key="item.id" class="flex">
                    <div @click="openModal(item.id)"
                        class="rounded-2xl text-primary bg-[#f9f6dc] border-8 border-primary p-5 text-center cursor-pointer w-full">
                        <!-- <img class="transition-transform duration-300 hover:scale-105" src="~/assets/images/gift-card.png" alt=""> -->
                        <h1 class="cinzel-decorative-font font-bold text-2xl md:text-2xl">Box #{{ item.id }}</h1>
                        <div class="bg-primary h-[2px]"></div>
                        <h1 class="md:text-xl font-extrabold merriweather-font">/{{ item.title }}/</h1>
                        <!-- <div class="bg-primary w-[90%] h-[2px] absolute top-[77px]"></div>
                        <div class="bg-primary w-[90%] h-[2px] absolute top-[107px]"></div> -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div v-if="showModal" class="fixed z-10 inset-0 flex items-center justify-center bg-black bg-opacity-50"
        @click.self="showModal = false">
        <div id="style-1"
            class="bg-white p-5 rounded-lg shadow-lg w-full max-w-3xl mx-4 relative overflow-y-auto max-h-[95vh]">
            <button @click="showModal = false" class="absolute top-5 right-5">
                <svg class="w-10" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                    <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                    <g id="SVGRepo_iconCarrier">
                        <path opacity="0.5"
                            d="M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12Z"
                            fill="#141414"></path>
                        <path
                            d="M8.96967 8.96967C9.26256 8.67678 9.73744 8.67678 10.0303 8.96967L12 10.9394L13.9697 8.96969C14.2626 8.6768 14.7374 8.6768 15.0303 8.96969C15.3232 9.26258 15.3232 9.73746 15.0303 10.0304L13.0607 12L15.0303 13.9696C15.3232 14.2625 15.3232 14.7374 15.0303 15.0303C14.7374 15.3232 14.2625 15.3232 13.9696 15.0303L12 13.0607L10.0304 15.0303C9.73746 15.3232 9.26258 15.3232 8.96969 15.0303C8.6768 14.7374 8.6768 14.2626 8.96969 13.9697L10.9394 12L8.96967 10.0303C8.67678 9.73744 8.67678 9.26256 8.96967 8.96967Z"
                            fill="#141414"></path>
                    </g>
                </svg>
            </button>
            <img class="w-24 mx-auto transition-transform duration-300 hover:scale-105"
                src="~/assets/images/gift-card.png" alt="">
            <h1 class="text-xl text-primary font-bold text-center my-3">/ {{ box.title }} /</h1>
            <h1 class="text-lg font-bold text-center font-dancing drop-shadow-lg ">From: {{ box.from }} <span
                    v-if="box.from_position">({{ box.from_position }})</span></h1>
            <p class="my-5" v-html="box.content"></p>

        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const showModal = ref(false);
const box: any = ref({});
const openModal = (id: number) => {
    box.value = arrayBoxs.find((item) => item.id === id);
    showModal.value = true;
}

const arrayBoxs = [
    {
        id: 1,
        title: 'A Letter After a Period of Reflection through My Eyes',
        from: 'Bao Vy',
        from_position: 'Head of Communications, CAM Project',
        content: `In the finite flow of time, within each fleeting moment we call "milestones of growth," I’ve come to understand what it means to "shine from your own energy." Do you know why I say this? In my eyes, you radiate a source of motivation—a drive for development. To put it more poetically, it’s the "light of knowledge." <br/> <div class="h-5"></div>
You are a petite young woman with an inspiring smile, but beyond that, you are someone with a spirit of "confidence, daring to think and daring to act." I see that spirit in the projects you undertake. You pour your heart and soul into something you call your "brainchild." You are passionate about everything, even when you stand on stage at a competition. Your image has become a source of motivation for so many who follow in your footsteps.<br/> <div class="h-5"></div>
You are a leader, a steadfast captain of the ship. You are strong and excel in everything you do. I hope that on your next journey, you will continue to seize even more opportunities. Most importantly, stay happy! Hehe.
`,
    },
    {
        id: 2,
        title: 'The Diligent Bee',
        from: 'Bao Vuong',
        from_position: 'A High School Friend',
        content: `To me, Boi Boi iis like a diligent bee in the club. You never shy away from difficult tasks and are always willing to help other members. Moreover, you consistently show a progressive attitude, eager to learn and explore new things.I believe that if you maintain this level of dedication, you will surely achieve great success.`,
    },
    {
        id: 3,
        title: 'Dare to Lead',
        from: 'Bach Tuyet',
        from_position: 'A Respected Senior',
        content: `I had the chance to meet and work with you during high school through various Youth Union activities. Back then, what impressed me the most about you was your dynamism, enthusiasm, and politeness. Additionally, your eagerness to grow and your love for learning made me admire you even more. You didn’t hesitate to message me with questions about studying or about the competitions and events I had participated in so you could gain experience and further develop yourself. Later, although we didn’t have as many opportunities to work together, I’ve continued to follow your journey from afar. You’re still the energetic girl I remember, but now you’ve grown into a more mature individual.<br/> <div class="h-5"></div>
Not only do you actively participate in events and clubs from school to provincial levels, but you also made me immensely proud to learn that you’ve become the leader of the first club at your high school. With your talent and determination, I have no doubt you’ll continue to achieve great successes and leave a meaningful mark on your journey.<br/> <div class="h-5"></div>
I wish you all the best—keep your passion alive and go even further on the path you’ve chosen!
`,
    },
    {
        id: 4,
        title: 'A Great Friend',
        from: 'Tran Duc Chinh',
        from_position: 'My close friend',
        content: `Boi Boi, a very special friend of mine. You are one of the most amazing people who has been part of my precious youth—someone who supported me a lot during my journey to the National Excellent Student Team. You are diligent and passionate about social activities, and honestly, you’re incredibly inspiring. With our three years of high school coming to an end, I hope we will always stay in touch, continue to see each other as great friends, and always smile at whatever life brings our way.`,
    },
    {
        id: 5,
        title: 'A Morning Glass of Water',
        from: 'Hoang Yen',
        from_position: 'My deskmate',
        content: `Boi and I have spent three years of high school together. Throughout our time studying and working on tasks together, I’ve come to see that Bội is someone who takes great responsibility for the assignments given by our teachers. Always cheerful and smiling in class, always enthusiastic about studying. What impresses me the most is your English proficiency—it’s something I truly admire. I’m so happy to have you as my friend. I hope we’ll have the chance to work together in the future and that our friendship will last forever.`,
    },
    {
        id: 6,
        title: 'A Long Dream',
        from: 'Hien Minh',
        from_position: 'Member of the CAM Project',
        content: `Hello, “boss”! Thank you for accompanying and guiding me throughout the past year. There’s so much I could say about you, but to sum it up: you’re beautiful, intelligent, caring, and incredibly talented. I was genuinely surprised when I first heard you speak English—it was so smooth, impressive, and captivating (especially that epic English speech during NGT’s Voice). I hope that in the journey ahead, you’ll shine even brighter and achieve even more success, just like your amazing and unforgettable name - Boi Boi.`,
    },
    {
        id: 7,
        title: 'Gratitude to the one who inspires',
        from: 'Ngoc Thi',
        from_position: 'Great supporter',
        content: `As I write these lines, I hope that you will understand my feelings and thoughts. Though it might sound a bit sentimental, these are the most sincere words I can express.<br/> <div class="h-5"></div>
Unlike many others, I have to admit that when I first met you, I wasn’t struck by a strong impression. The image of Boi in my mind was simply of an older sister who was chosen to deliver the speech on the opening day of the school year, with the signature opening line, "Have you had breakfast yet?" (which I found quite unique). Perhaps it was because I didn’t fully understand who you were, nor could I see all the value you brought to others. However, fate intervened, and I decided to join a group in the club where you were the president. Through that, we had many opportunities to work together. The more I got to know you, the more I saw your dedication and how you approached work and life, and I began to realize a clear difference in your character. You’re not only someone with solid expertise but also a "doer," full of ambition and with your own clear opinions. These qualities made you stand out even more, as a living example of the saying, "Those who have dreams will shine with their own light."<br/> <div class="h-5"></div>
In contrast, I would describe myself as someone with ambitions piled up somewhere, but never daring to pursue them, thinking they were just idle dreams. These thoughts have held me back from reaching my true potential. This is why, to me, you have become an unexpected source of inspiration. It would not be an exaggeration to say that you have played a significant role in my growth. You introduced me to many competitions, opportunities, and activities, opening many doors for me to test myself and interact with people much more outstanding than I ever imagined. Thanks to you, I have experienced both failures and the sweet rewards of success. To me, all of this has been a fascinating journey, and you have always been by my side, encouraging me every step of the way.<br/> <div class="h-5"></div>
As the days passed, we became closer. Beyond the opportunities you provided, what surprised me most about you was your thoughtful and caring nature. Although you may seem carefree and detached at times, on the day of my birthday, you made me see things differently (How mysterious you are!). I don’t usually celebrate my birthday, and I’m already touched when a few close friends wish me well. On that day, you teased me, saying, "There’s no gift for you!" I just laughed it off, thinking nothing of it. But to my surprise, you actually had a gift for me. I was deeply moved, and at that moment, I thought, "When it’s your birthday, I will give you an amazing gift!" I honestly spent a long time choosing the perfect gift for you.<br/> <div class="h-5"></div>
After all we’ve been through together, I now truly see you as an older sister, someone I deeply cherish and respect. Even though we may not meet as often as we did during high school, I still hope we’ll stay in touch. I am grateful to fate for bringing me to you! I’ve shared enough for now, and I wish you all the success in your new journey.
`,
    },
    {
        id: 8,
        title: 'A LETTER FROM BEAUTIFUL MEMORIES',
        from: 'Xuan Quynh',
        from_position: 'Head of the Communications Department of DFL',
        content: `Boi Boi has always been a young girl who deeply impressed me, right from the first time we worked together during the challenge round of the project. Your enthusiasm, joy, and creativity shone through from the very beginning, but what I truly value is your hard working spirit, dedication, and relentless effort. After nearly a year of working together, both I and the rest of the team at “Lop Hoc Diu Dang” were often amazed by your unique, creative ideas and your wholehearted contribution, even though you had to balance your university entrance exam preparation and participate in challenging public speaking competitions. To me, you have always been a lovely and admirable teammate, always willing to support the project, even though we no longer work together in the same way as before. I believe that with your dedication and determination, you will go far on the journey you have chosen. I wish you continued success and brilliance in the future!`,
    },
    {
        id: 9,
        title: 'A Refreshing Glass of Soda',
        from: 'Nghi',
        from_position: 'My classmate',
        content: `Here are some of my personal thoughts about Bội Bội during the time we studied together. From the first time we met, I was deeply impressed by how intelligent and active Bội was in all school and class activities. Later, when we worked together, I saw how serious and dedicated Boi was - a great team leader who assigned tasks fairly and efficiently. It felt so reliable to collaborate with Boi, thanks to her creativity. I was also super impressed by her enthusiasm and the endless positive energy she brought!`,
    },
    {
        id: 10,
        title: 'A Crunchy Bag of Potato Chips',
        from: 'Dinh Duy',
        from_position: 'Junior',
        content: `My first impression of you was when we went to watch the Literature Club at Dien Hong Cultural House together, introduced by a classmate. At school, I knew you as someone very active, but we hadn’t interacted much before that. When we got to Dien Hong, I sat near you, and we started chatting—sharing our names, classes, and even competing a bit over achievements, haha. What left a lasting impression on me was your humorous, energetic personality and your playful competitive streak, which I found really interesting.<br/> <div class="h-5"></div>
You were also the one who introduced me to and guided me through the academic competition “Road to success”. Before meeting you, I thought you were introverted and quiet, but after getting to know you, I realized you’re super outgoing and talkative—but in the most adorable way!<br/> <div class="h-5"></div>
Thank you for being my friend!
`,
    },
    {
        id: 11,
        title: 'A Secret Letter',
        from: 'Ha Duy',
        from_position: 'My friend from middle school to high school',
        content: `This is a small letter for you. If I had to describe you in one word, "perfect" would probably be the most fitting. We’ve known each other for a long time, and we’ve had many opportunities to collaborate on various projects. Honestly, I’ve never met anyone with such excellent teamwork skills, someone so thorough in every step of preparation, and so meticulous in planning every detail, no matter how small. You lead the team incredibly well.<br/> <div class="h-5"></div>
You’re like the one who creates "instant noodles" - just relying on well-prepared content, making team collaboration so much easier. From being an introvert, now I’m able to express what I want to convey, though sometimes I still feel a bit passive =)). Your greatest strength is your ability to work in teams. You can easily capture people's attention, speak fluently and smoothly, and are so energetic. So, keep honing and leveraging your strengths, and don’t listen to anyone who doubts you because right now, you’re doing an amazing job. Keep looking ahead, build a strong shield for yourself, and become the best version of yourself.
`,
    },
    {
        id: 12,
        title: 'Tiny words with love from TĐ',
        from: 'Dang Dan',
        from_position: 'A friend I met by chance at MUN',
        content: `Your gentle, cute, and pretty appearance made it easier for me to talk to her and approach her for the first time. Although I'm extroverted, I sometimes feel shy about starting a conversation with certain people. However, when I saw her being friendly and cute, I decided to get closer, and she really was friendly. Supportive, responsible, and trustworthy are three words I would use to describe her. Although I haven’t had many experiences with her yet, up until now, I’ve always felt warmth and gentleness from the way she treats me and everyone else.`,
    },
    {
        id: 13,
        title: 'Unforgettable moment',
        from: 'Tu',
        from_position: 'An older brother who participated in the charity event',
        content: `Hello Boi Boi, a young, dynamic, passionate girl full of youthful energy. The first time I met you was during a charity event in Song Hinh. Honestly, at first, I thought you were probably around my age or older. Then, I started to be impressed by you when it was lunchtime. I was helping the kids get food and didn’t notice you, but when you called out “chú chú,” I thought you were calling my name. When I turned around, I saw you with your two friends, and at that moment, I was casually impressed by you.<br/> <div class="h-5"></div>
In the afternoon, when everyone started preparing the event, I saw you helping in the kitchen, looking very busy. During the opening ceremony, I saw you playing with the kids a lot, and throughout the day, you did so many things but still had enough energy, always with a smile on your face, which gave me the motivation to continue helping. I was also quite impressed with your proactive enthusiasm during the event.`,
    },
    {
        id: 14,
        title: 'My sunshine',
        from: 'Anh Nguyen Nu Hoang',
        from_position: '',
        content: `My name is Anh Nguyen Nu Hoang, and I am a freshman at the University of Kansas, USA, where I was awarded a $48,000 scholarship for my four-year undergraduate program. I have had the privilege of working alongside Boi Boi on various community projects and extracurricular activities, and she has consistently impressed me with her leadership, creativity, and dedication. As the president of her school’s organization, she excels at uniting people and fostering collaboration to achieve common goals.<br/> <div class="h-5"></div>
What I love most about Boi Boi is her passion for communication and her long-held dream of studying in the United States. She constantly seeks opportunities to enhance her skills, both professionally and personally, through relentless learning and self-improvement. One memorable instance was when she led a project under unexpected circumstances and, through her resourcefulness and composure, turned it into a resounding success. I am confident that Boi Boi will make an outstanding contribution to any academic or professional environment.`,
    },
    {
        id: 15,
        title: 'A message from lord of deadlines',
        from: '',
        from_position: '',
        content: `First of all, Huy feels very lucky to have worked with Pội during DTEC GEN 1. Although the time working together wasn’t very long, Huy found many impressive qualities in Pội. In terms of personality, Pội is a sweet, friendly, and wise friend who always smiles and never gives up. As for her working style, Pội is highly self-disciplined and consistently completes her assigned tasks with meticulous care and thoroughness. In addition, she has extensive experience as a volunteer in various events and has reaped great rewards from those efforts. Wishing Pội everything except hardships ❤️‍🔥`,
    },
    {
        id: 16,
        title: 'You’re wonderful',
        from: 'Van Anh',
        from_position: 'Head of Marketing department of YE-MUN',
        content: `Dear Bội Bội, <br/> <div class="h-5"></div>
        Through the times we participated in activities and community projects together, I’ve been deeply impressed by your sense of responsibility, enthusiasm, and dedication. You not only excel at completing your own tasks but also embrace challenges and consistently spread positivity to those around you. <br/> <div class="h-5"></div>
        With your perseverance and determined attitude toward work, I firmly believe that your continuous efforts will take you even further, allowing you to achieve many remarkable accomplishments in the future. Wishing you good health and success in reaching your dreams.<br/> <div class="h-5"></div>
        Warm regards!`,
    },
    {
        id: 17,
        title: 'The Light of Passion and Dedication',
        from: '',
        from_position: '',
        content: `Although I haven’t known you, Boi, for very long and haven’t had many chances to interact with you outside of the time we were in the UNICEF council together at YE-MUN, I truly admire you for so many things!!! My first impression (just from seeing you on social media before actually meeting you) was that you are super energetic, participating in so many extracurricular activities and competitions both inside and outside of school (and always achieving high results =))). I couldn’t help but wonder how someone can manage their time so well to excel in both academics and extracurriculars.<br/> <div class="h-5"></div>
        What I respect even more about you are the volunteer activities you take part in because I can see that you genuinely want to spread happiness to society. That’s something I really want to do too, but I haven’t had the chance to try yet, huhuu. The times I’ve met you in person can be counted on one hand, but they’ve all been super fun memories.<br/> <div class="h-5"></div>
        During YE-MUN, I could see your passion and determination through every speech and debate you had with other delegates. You stood strong to defend your bloc’s viewpoint, and honestly, I was so impressed that I got goosebumps!!! That’s how serious you are during meetings, but in real life, you’re so friendly and cheerful, which made our end-of-event party a blast hehe 😋.<br/> <div class="h-5"></div>
        By the way, I wish your projects great success, and I hope all the amazing things you deserve will come your way, Boi Boi. Best wishes ❤`,
    },
]
</script>

<style scoped></style>