<script lang="ts">
	import { onMount } from 'svelte';

	let scrollY = 0;
</script>

<svelte:window bind:scrollY />

<div class="font-sans text-gray-900 antialiased selection:bg-orange-200 selection:text-orange-900">
	<!-- Navigation / Header -->
	<header class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
		<div class="px-6 md:px-12 lg:px-24 py-4 flex items-center justify-between">
			<a href="/" class="flex items-center gap-2">
				<svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-gray-900">
					<path
						fill-rule="evenodd"
						clip-rule="evenodd"
						d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
						fill="currentColor"
					/>
				</svg>
				<span class="font-semibold text-xl">Base</span>
			</a>
			<nav class="hidden md:flex items-center gap-8">
				<a href="#how-it-works" class="text-sm text-gray-600 hover:text-gray-900 transition-colors">How it works</a>
				<a href="#for-companies" class="text-sm text-gray-600 hover:text-gray-900 transition-colors">For companies</a>
				<a href="#join" class="px-4 py-2 bg-gray-900 text-white rounded-lg text-sm font-medium hover:bg-gray-800 transition-colors">Join Base</a>
			</nav>
		</div>
	</header>

	<!-- Hero Section -->
	<section class="relative min-h-screen w-full bg-gray-950 text-white px-6 md:px-12 lg:px-24 pt-32 pb-24 flex flex-col justify-center">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center max-w-7xl mx-auto">
			<div class="space-y-8">
				<h1 class="font-serif text-5xl md:text-6xl lg:text-7xl leading-[1.1] tracking-tight">
					Beyond networking. <br />
					<span class="text-primary-400">Meaningful connections.</span>
				</h1>
				<p class="text-xl text-gray-300 leading-relaxed max-w-xl">
					Base connects professionals to curated gatherings through personality matching and archetype-based curation for conversations that matter.
				</p>
				<div class="flex flex-col sm:flex-row gap-4">
					<a href="#join" class="inline-flex items-center justify-center px-8 py-4 bg-primary-500 text-white rounded-lg text-base font-medium hover:bg-primary-600 transition-colors duration-300">
						Join Base
					</a>
					<a href="#how-it-works" class="inline-flex items-center justify-center px-8 py-4 border border-white/30 rounded-lg text-base font-medium hover:bg-white hover:text-gray-900 transition-colors duration-300">
						How it works
					</a>
				</div>
			</div>
			<div class="relative h-[500px] rounded-2xl overflow-hidden">
				<img src="/generated/image-diverse-group-of-professionals-having-an-1765829615602-0.webp" alt="Professionals engaged in meaningful conversation" class="w-full h-full object-cover" />
			</div>
		</div>
	</section>

	<!-- Social Proof -->
	<section class="bg-white px-6 md:px-12 lg:px-24 py-16 md:py-24">
		<div class="max-w-5xl mx-auto text-center space-y-12">
			<p class="text-lg md:text-xl text-gray-600">Trusted by leading companies for corporate wellness programs</p>
			
			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-12">
				<div class="space-y-2">
					<div class="text-4xl md:text-5xl font-bold text-gray-900">500+</div>
					<p class="text-gray-600">Professionals matched</p>
				</div>
				<div class="space-y-2">
					<div class="text-4xl md:text-5xl font-bold text-gray-900">200+</div>
					<p class="text-gray-600">Curated gatherings</p>
				</div>
				<div class="space-y-2">
					<div class="text-4xl md:text-5xl font-bold text-gray-900">95%</div>
					<p class="text-gray-600">Would recommend</p>
				</div>
			</div>
		</div>
	</section>

    <!-- How It Works Section -->
    <section class="bg-gray-50 px-6 md:px-12 lg:px-24 py-12 md:py-24" id="how-it-works">
        <div class="max-w-6xl mx-auto">
            <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900 mb-16 text-center">How Base works</h2>

            <div class="space-y-24 md:space-y-32">
                <!-- Step 1: Discover -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="space-y-6 order-2 lg:order-1">
                        <div class="inline-block px-4 py-2 bg-primary-100 text-primary-700 rounded-full text-sm font-medium">Step 1</div>
                        <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Discover your archetype</h3>
                        <p class="text-gray-600 text-lg leading-relaxed">
                            Take our personality assessment to understand your conversation style, interests, and what makes you thrive in social settings. Our algorithm identifies your unique archetype to ensure meaningful matches.
                        </p>
                    </div>
                    <div class="order-1 lg:order-2">
                        <div class="aspect-[4/3] bg-gradient-to-br from-primary-50 to-primary-100 rounded-2xl overflow-hidden relative flex items-center justify-center p-12">
                            <div class="grid grid-cols-2 gap-4 w-full max-w-sm">
                                <div class="bg-white rounded-xl p-6 shadow-sm">
                                    <div class="w-12 h-12 bg-primary-200 rounded-full mb-3"></div>
                                    <div class="h-2 bg-gray-200 rounded w-3/4"></div>
                                </div>
                                <div class="bg-white rounded-xl p-6 shadow-sm">
                                    <div class="w-12 h-12 bg-primary-300 rounded-full mb-3"></div>
                                    <div class="h-2 bg-gray-200 rounded w-3/4"></div>
                                </div>
                                <div class="bg-white rounded-xl p-6 shadow-sm">
                                    <div class="w-12 h-12 bg-primary-400 rounded-full mb-3"></div>
                                    <div class="h-2 bg-gray-200 rounded w-3/4"></div>
                                </div>
                                <div class="bg-white rounded-xl p-6 shadow-sm">
                                    <div class="w-12 h-12 bg-primary-500 rounded-full mb-3"></div>
                                    <div class="h-2 bg-gray-200 rounded w-3/4"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Step 2: Match -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="aspect-[4/3] bg-gray-900 rounded-2xl overflow-hidden relative">
                        <img src="/generated/image-group-dinner-gathering-with-professional-1765829910008-1.webp" alt="Curated gathering" class="w-full h-full object-cover" />
                    </div>
                    <div class="space-y-6">
                        <div class="inline-block px-4 py-2 bg-primary-100 text-primary-700 rounded-full text-sm font-medium">Step 2</div>
                        <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Get matched to gatherings</h3>
                        <p class="text-gray-600 text-lg leading-relaxed">
                            Our curation engine matches you with small groups of 6-8 professionals who share complementary archetypes and interests. Every gathering is designed for depth, not breadth.
                        </p>
                    </div>
                </div>

                <!-- Step 3: Connect -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="space-y-6 order-2 lg:order-1">
                        <div class="inline-block px-4 py-2 bg-primary-100 text-primary-700 rounded-full text-sm font-medium">Step 3</div>
                        <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Connect over dinner</h3>
                        <p class="text-gray-600 text-lg leading-relaxed">
                            Join curated dinners at carefully selected venues. Facilitated conversation prompts ensure everyone engages meaningfully. Leave with genuine connections, not just business cards.
                        </p>
                    </div>
                    <div class="order-1 lg:order-2">
                        <div class="aspect-[4/3] bg-primary-950 rounded-2xl overflow-hidden relative flex items-center justify-center p-8">
                            <div class="relative w-full max-w-md">
                                <div class="absolute inset-0 bg-primary-500/20 rounded-full blur-3xl"></div>
                                <div class="relative bg-white rounded-2xl p-8 shadow-2xl">
                                    <div class="flex items-center gap-4 mb-6">
                                        <div class="w-16 h-16 bg-primary-200 rounded-full"></div>
                                        <div class="flex-1">
                                            <div class="h-3 bg-gray-200 rounded w-3/4 mb-2"></div>
                                            <div class="h-2 bg-gray-100 rounded w-1/2"></div>
                                        </div>
                                    </div>
                                    <div class="space-y-3">
                                        <div class="h-2 bg-gray-100 rounded"></div>
                                        <div class="h-2 bg-gray-100 rounded w-5/6"></div>
                                        <div class="h-2 bg-gray-100 rounded w-4/6"></div>
                                    </div>
                                    <div class="mt-6 flex gap-2">
                                        <div class="flex-1 h-10 bg-primary-100 rounded-lg"></div>
                                        <div class="flex-1 h-10 bg-gray-100 rounded-lg"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Value Props Section -->
    <section class="bg-white px-6 md:px-12 lg:px-24 py-12 md:py-24">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900 mb-16 max-w-3xl text-center mx-auto">Why professionals choose Base</h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
            <!-- Curated -->
            <div class="bg-gray-50 p-8 rounded-2xl hover:shadow-lg transition-shadow duration-300 flex flex-col h-full">
                <div class="w-14 h-14 bg-primary-100 rounded-xl flex items-center justify-center mb-6">
                    <svg class="w-7 h-7 text-primary-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
                <h3 class="text-xl font-semibold mb-4">Curated matching</h3>
                <p class="text-gray-600 leading-relaxed">
                    No more awkward small talk. Our algorithm pairs you with professionals who share your intellectual curiosity and conversation style.
                </p>
            </div>

            <!-- Quality -->
            <div class="bg-gray-50 p-8 rounded-2xl hover:shadow-lg transition-shadow duration-300 flex flex-col h-full">
                <div class="w-14 h-14 bg-primary-100 rounded-xl flex items-center justify-center mb-6">
                    <svg class="w-7 h-7 text-primary-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path>
                    </svg>
                </div>
                <h3 class="text-xl font-semibold mb-4">Quality over quantity</h3>
                <p class="text-gray-600 leading-relaxed">
                    Small groups of 6-8 people ensure everyone has space to contribute. Leave with meaningful connections, not a stack of business cards.
                </p>
            </div>

            <!-- Depth -->
            <div class="bg-gray-50 p-8 rounded-2xl hover:shadow-lg transition-shadow duration-300 flex flex-col h-full">
                <div class="w-14 h-14 bg-primary-100 rounded-xl flex items-center justify-center mb-6">
                    <svg class="w-7 h-7 text-primary-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
                    </svg>
                </div>
                <h3 class="text-xl font-semibold mb-4">Intellectual depth</h3>
                <p class="text-gray-600 leading-relaxed">
                    Facilitated prompts and archetype-based curation ensure conversations go beyond surface level. Discuss ideas that matter.
                </p>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="bg-gray-50 px-6 md:px-12 lg:px-24 py-12 md:py-24">
        <div class="max-w-6xl mx-auto">
            <h2 class="font-serif text-3xl md:text-4xl text-gray-900 mb-16 text-center">What members are saying</h2>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-white rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow duration-300">
                    <div class="flex items-center gap-4 mb-6">
                        <img src="/generated/image-professional-woman-in-her-30s-smiling-wa-1765829618359-3.webp" alt="Sarah Chen" class="w-16 h-16 rounded-full object-cover" />
                        <div>
                            <h4 class="font-semibold text-gray-900">Sarah Chen</h4>
                            <p class="text-sm text-gray-500">Product Manager, Tech</p>
                        </div>
                    </div>
                    <p class="text-gray-600 leading-relaxed">
                        "Finally, networking that doesn't feel transactional. I've had more meaningful conversations in one Base dinner than in years of industry events."
                    </p>
                </div>

                <!-- Testimonial 2 -->
                <div class="bg-white rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow duration-300">
                    <div class="flex items-center gap-4 mb-6">
                        <img src="/generated/image-professional-man-in-his-40s-confident-an-1765829621059-4.webp" alt="Michael Rodriguez" class="w-16 h-16 rounded-full object-cover" />
                        <div>
                            <h4 class="font-semibold text-gray-900">Michael Rodriguez</h4>
                            <p class="text-sm text-gray-500">Strategy Consultant</p>
                        </div>
                    </div>
                    <p class="text-gray-600 leading-relaxed">
                        "The archetype matching is brilliant. Every person at my table brought a unique perspective, but we all clicked instantly. This is what professional connection should be."
                    </p>
                </div>

                <!-- Testimonial 3 -->
                <div class="bg-white rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow duration-300">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="w-16 h-16 rounded-full bg-primary-200 flex items-center justify-center">
                            <span class="text-2xl font-semibold text-primary-700">JL</span>
                        </div>
                        <div>
                            <h4 class="font-semibold text-gray-900">Jennifer Lee</h4>
                            <p class="text-sm text-gray-500">Creative Director</p>
                        </div>
                    </div>
                    <p class="text-gray-600 leading-relaxed">
                        "I was skeptical at first, but Base delivered. The conversations were deep, the people were genuine, and I left with connections I actually want to maintain."
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- For Companies Section -->
    <section class="px-6 md:px-12 lg:px-24 py-12 md:py-24" id="for-companies">
        <div class="bg-gray-950 rounded-3xl p-8 md:p-16 lg:p-20 max-w-6xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-white">Corporate wellness that works</h3>
                    <p class="text-gray-300 text-lg leading-relaxed">
                        Base partners with forward-thinking companies to combat networking fatigue and build genuine connections among your teams. Our curated intellectual dinners are the antidote to superficial corporate events.
                    </p>
                    <ul class="space-y-3 text-gray-300">
                        <li class="flex items-start gap-3">
                            <svg class="w-6 h-6 text-primary-400 flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                            </svg>
                            <span>Reduce employee isolation and burnout</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <svg class="w-6 h-6 text-primary-400 flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                            </svg>
                            <span>Foster cross-departmental collaboration</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <svg class="w-6 h-6 text-primary-400 flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                            </svg>
                            <span>Strengthen company culture through meaningful connection</span>
                        </li>
                    </ul>
                    <div class="pt-4">
                        <a href="#contact" class="inline-flex items-center justify-center px-8 py-4 bg-primary-500 text-white rounded-lg text-base font-medium hover:bg-primary-600 transition-colors duration-300">
                            Partner with Base
                        </a>
                    </div>
                </div>
                <div class="relative h-[400px] rounded-2xl overflow-hidden bg-gray-900">
                    <div class="absolute inset-0 bg-gradient-to-br from-primary-500/20 to-transparent"></div>
                    <div class="absolute inset-0 flex items-center justify-center p-8">
                        <div class="grid grid-cols-2 gap-4 w-full max-w-sm">
                            <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20">
                                <div class="text-3xl font-bold text-white mb-2">85%</div>
                                <div class="text-sm text-gray-300">Employee satisfaction</div>
                            </div>
                            <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20">
                                <div class="text-3xl font-bold text-white mb-2">3x</div>
                                <div class="text-sm text-gray-300">Cross-team connections</div>
                            </div>
                            <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 col-span-2">
                                <div class="text-3xl font-bold text-white mb-2">92%</div>
                                <div class="text-sm text-gray-300">Would attend again</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Constellations (Footer Hero) -->
    <section class="relative bg-gradient-to-b from-[#e69d75] via-[#c46d5e] to-[#8b3a2b] pt-32 pb-48 px-6 md:px-12 lg:px-24 overflow-hidden">
        <div class="max-w-5xl relative z-10">
            <h2 class="font-serif text-4xl md:text-6xl lg:text-7xl text-[#fdfbf7] leading-tight mb-8">
                All our constellations, under one sky. <br />
                <span class="text-[#fdfbf7]/70">Find out how we chart the path from idea to icon — through strategy, creation, building, and scaling — turning the unseeable into the undeniable.</span>
            </h2>
            
            <div class="mt-16">
                 <a href="/approach" class="inline-flex items-center justify-center px-6 py-3 border border-white/30 rounded-full text-sm font-medium text-white hover:bg-white hover:text-[#8b3a2b] transition-colors duration-300 backdrop-blur-sm">
                    Our Approach
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#3e1c16] text-[#eaddcf] px-6 md:px-12 lg:px-24 pt-24 pb-12 relative overflow-hidden">
        
        <!-- Large Flower Image Overlapping Sections -->
        <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 translate-y-0 w-[800px] h-[1000px] pointer-events-none z-0 opacity-90 mix-blend-hard-light">
             <img src="https://images.unsplash.com/photo-1596294399224-b174780e816e?q=80&w=1000&auto=format&fit=crop" alt="Hibiscus Flower" class="w-full h-full object-contain" />
        </div>

        <div class="relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-24">
                <div class="col-span-1 md:col-span-2">
                    <a href="/contact" class="text-2xl font-medium hover:opacity-80 transition-opacity inline-flex items-center">
                        Work with us <span class="ml-2">→</span>
                    </a>
                </div>
                
                <div class="space-y-4">
                    <h4 class="font-medium text-white">London, UK</h4>
                    <p class="text-sm opacity-70">5:20 am</p>
                    <div class="pt-4 text-sm opacity-70 space-y-1">
                        <p>london@newgenre.studio</p>
                        <p>+44 20 4572 6788</p>
                        <p class="mt-4">2 Appleby Yard,<br>Seames Walk,<br>London SE10 0BU, UK</p>
                    </div>
                </div>

                <div class="space-y-4">
                    <h4 class="font-medium text-white">San Francisco</h4>
                    <p class="text-sm opacity-70">9:20 pm</p>
                    <div class="pt-4 text-sm opacity-70 space-y-1">
                        <p>sf@newgenre.studio</p>
                        <p>+1 650 466 6274</p>
                    </div>
                </div>
            </div>

            <div class="flex flex-col md:flex-row justify-between items-end border-t border-white/10 pt-8">
                <div class="mb-4 md:mb-0">
                    <!-- Logo Icon -->
                    <svg width="32" height="32" viewBox="0 0 24 24" fill="currentColor" class="text-white">
                        <rect x="2" y="2" width="9" height="9" rx="2" />
                        <rect x="13" y="2" width="9" height="9" rx="2" />
                        <rect x="2" y="13" width="9" height="9" rx="2" />
                        <rect x="13" y="13" width="9" height="9" rx="2" />
                    </svg>
                </div>
                
                <div class="flex gap-6 text-xs font-medium">
                    <a href="#" class="hover:text-white transition-colors">LinkedIn</a>
                    <a href="#" class="hover:text-white transition-colors">Instagram</a>
                    <a href="#" class="hover:text-white transition-colors">X</a>
                    <a href="#" class="hover:text-white transition-colors">Join Us</a>
                </div>
            </div>

            <div class="flex justify-between text-[10px] opacity-50 mt-12">
                <p>© 2025 New Genre</p>
                <p>Privacy</p>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom utility for vertical writing mode */
    .writing-vertical-rl {
        writing-mode: vertical-rl;
    }
</style>

