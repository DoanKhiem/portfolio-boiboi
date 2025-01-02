<template>
	<NuxtLayout>
		<div class="container mx-auto">
			<NuxtPage />
		</div>

		<div class="back-arrow bg-primary" @click="backArrow">
			<svg fill="#d7a947" class="md:w-6 md:h-6 w-4 h-4" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg"
				xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 26.676 26.676" xml:space="preserve">
				<g id="SVGRepo_bgCarrier" stroke-width="0"></g>
				<g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
				<g id="SVGRepo_iconCarrier">
					<g>
						<path
							d="M26.105,21.891c-0.229,0-0.439-0.131-0.529-0.346l0,0c-0.066-0.156-1.716-3.857-7.885-4.59 c-1.285-0.156-2.824-0.236-4.693-0.25v4.613c0,0.213-0.115,0.406-0.304,0.508c-0.188,0.098-0.413,0.084-0.588-0.033L0.254,13.815 C0.094,13.708,0,13.528,0,13.339c0-0.191,0.094-0.365,0.254-0.477l11.857-7.979c0.175-0.121,0.398-0.129,0.588-0.029 c0.19,0.102,0.303,0.295,0.303,0.502v4.293c2.578,0.336,13.674,2.33,13.674,11.674c0,0.271-0.191,0.508-0.459,0.562 C26.18,21.891,26.141,21.891,26.105,21.891z">
						</path>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
						<g> </g>
					</g>
				</g>
			</svg>
		</div>

		<div class="scroll-top bg-primary" @click="scrollToTop">
			<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"
				class="md:w-6 md:h-6 w-4 h-4">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 15l7-7 7 7" />
			</svg>
		</div>
	</NuxtLayout>
</template>

<script setup lang="ts">
const scrollToTop = () => {
	window.scrollTo({ top: 0, behavior: 'smooth' });
};
const backArrow = () => {
	window.history.back();
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Crimson+Pro:ital,wght@0,200..900;1,200..900&family=Pacifico&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&family=Nunito:ital,wght@0,200..1000;1,200..1000&family=Yeseva+One&display=swap');

.yeseva-one-font {
	font-family: "Yeseva One", cursive;
	font-style: normal;
}

.nunito-font {
	font-family: "Nunito", sans-serif;
	font-style: normal;
}

.cinzel-decorative-font {
	font-family: "Cinzel Decorative", serif;
	/* font-weight: 400; */
	font-style: normal;
}

.merriweather-font {
	font-family: "Merriweather", serif;
	/* font-weight: 400; */
	font-style: normal;
}

.abril-fatface-regular-font {
	font-family: "Abril Fatface", serif;
	font-weight: 400;
	font-style: normal;
}

.pacifico-regular-font {
	font-family: "Pacifico", cursive;
	font-weight: 400;
	font-style: normal;
}

.crimson-pro-font {
	font-family: "Crimson Pro", serif;
	font-optical-sizing: auto;
	font-style: normal;
}


.scroll-top {
	position: fixed;
	bottom: 20px;
	right: 20px;
	color: #d7a947;
	padding: 10px;
	border-radius: 50%;
	cursor: pointer;
	transition: opacity 0.3s;

	animation-name: bounce;
	animation-delay: 1s;
	animation-duration: 2s;
	animation-iteration-count: infinite;
}

.back-arrow {
	position: fixed;
	bottom: 20px;
	left: 20px;
	color: #d7a947;
	padding: 10px;
	border-radius: 50%;
	cursor: pointer;
	transition: opacity 0.3s;

	animation-name: bounce;
	animation-delay: 1s;
	animation-duration: 2s;
	animation-iteration-count: infinite;
}

@keyframes bounce {

	0%,
	100%,
	20%,
	50%,
	80% {
		-webkit-transform: translateY(0);
		-ms-transform: translateY(0);
		transform: translateY(0);
	}

	40% {
		-webkit-transform: translateY(-30px);
		-ms-transform: translateY(-30px);
		transform: translateY(-30px);
	}

	60% {
		-webkit-transform: translateY(-15px);
		-ms-transform: translateY(-15px);
		transform: translateY(-15px);
	}
}
</style>
