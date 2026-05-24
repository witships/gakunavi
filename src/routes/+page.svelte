<script lang="ts">
	const workshops = [
		{
			title: '国語',
			desc: '撮影・編集・演出まで、オリジナル動画をつくろう！',
			icon: '📹',
			image: '/images/workshop-video.webp'
		},
		{
			title: '数学',
			desc: '画像生成やAIツールを使って、アイデアをカタチに！',
			icon: '🎨',
			image: '/images/workshop-ai.webp'
		},
		{
			title: '英語',
			desc: 'アイデアを出し合い、オリジナルゲームを企画・制作！',
			icon: '🎮',
			image: '/images/workshop-game.webp'
		},
		{
			title: '理科',
			desc: '企画・撮影・編集・発信まで、人気YouTuberの流れを体験！',
			icon: '🎥',
			image: '/images/workshop-youtuber.webp'
		},
		{
			title: '社会',
			desc: '企画・撮影・編集・発信まで、人気YouTuberの流れを体験！',
			icon: '🎥',
			image: '/images/workshop-youtuber.webp'
		},
		{
			title: '情報',
			desc: '企画・撮影・編集・発信まで、人気YouTuberの流れを体験！',
			icon: '🎥',
			image: '/images/workshop-youtuber.webp'
		}
	];

	const steps = [
		{
			step: '01',
			title: '無料体験に申し込む',
			desc: 'フォームから簡単に申し込み！まずは気軽に体験しよう。',
			icon: '📝'
		},
		{
			step: '02',
			title: '好きなワークショップを選ぶ',
			desc: '興味のあるテーマを選んで、自分のペースで参加！',
			icon: '🔍'
		},
		{
			step: '03',
			title: '仲間とつくって、発表する',
			desc: 'チームで作品をつくり、発表会でシェアしよう！',
			icon: '🙌'
		}
	];

	const members = [
		{
			name: 'ハルミナ',
			grade: '中学2年生',
			comment: '苦手だった数学が好きになりました。',
			avatar: '/images/harumina.webp'
		},
		{
			name: 'ラギオ',
			grade: '中学1年生',
			comment: '将来の夢が見つかりました！',
			avatar: '/images/ragio.webp'
		},
		{
			name: 'yoshiken',
			grade: '中学3年生',
			comment: '自宅からでも友達と一緒に学べて楽しい！',
			avatar: '/images/yoshiken.webp'
		}
	];
</script>

<svelte:head>
	<title>がくなび | AIとつながる、創造の放課後ラボ</title>
</svelte:head>

<div class="font-body min-h-screen bg-white font-sans text-slate-800">
	<!-- Header -->
	<header
		class="sticky top-0 z-50 flex items-center justify-between border-b border-slate-100 bg-white/80 px-6 py-4 backdrop-blur-md"
	>
		<div class="flex items-center gap-2">
			<img src="/images/favicon.png" alt="logo" class="h-12 rounded-2xl" />
			<h1 class="text-xl font-bold tracking-tight text-blue-900">がくなび</h1>
		</div>
		<nav class="hidden items-center gap-8 text-sm font-medium text-slate-600 md:flex">
			<a href="#about" class="hover:text-primary">がくなびについて</a>
			<a href="#workshops" class="hover:text-primary">学べるコース</a>
			<a href="#steps" class="hover:text-primary">学習の進め方</a>
			<a href="#members" class="hover:text-primary">ギルドメンバー</a>
			<a href="#faq" class="hover:text-primary">よくある質問</a>
		</nav>
		<div class="flex items-center gap-4">
			<button
				class="rounded-full border border-primary px-4 py-2 text-sm font-bold text-primary hover:bg-blue-50"
				>ログイン</button
			>
			<button
				class="rounded-full bg-primary px-6 py-2 text-sm font-bold text-white shadow-lg shadow-blue-200 transition-all hover:scale-105"
				>無料体験に申し込む ＞</button
			>
		</div>
	</header>

	<!-- Hero Section -->
	<section
		class="hero relative overflow-hidden bg-linear-to-br from-blue-50 to-white px-6 py-20 lg:px-20"
	>
		<div class="mx-auto flex max-w-7xl flex-col items-center gap-12 lg:flex-row">
			<div class="flex-1 space-y-8 text-center lg:text-left">
				<h2 class="text-5xl leading-tight font-black text-slate-900 lg:text-7xl">
					“<span class="text-primary">好き</span>”をつなげて、<br />
					<span class="font-extrabold text-secondary italic">未来</span> をつくろう。
				</h2>
				<p class="mx-auto max-w-2xl text-lg leading-relaxed text-slate-600 lg:mx-0">
					がくなびは、自分のペースで学べるオンライン学習。
				</p>
				<div class="grid grid-cols-1 gap-4 py-4 text-sm font-bold md:grid-cols-3">
					<div
						class="flex items-center justify-center gap-2 rounded-xl border border-blue-100 bg-white p-3 text-blue-800 shadow-sm lg:justify-start"
					>
						<span class="text-lg">🏫</span> 自分のペースで学ぶも良し
					</div>
					<div
						class="flex items-center justify-center gap-2 rounded-xl border border-green-100 bg-white p-3 text-green-800 shadow-sm lg:justify-start"
					>
						<span class="text-lg">🤖</span> セミナー形式でみんなと一緒に学ぶも良し
					</div>
				</div>
				<div class="flex flex-col items-center gap-4 pt-4 lg:items-start">
					<button
						class="rounded-full bg-primary px-12 py-5 text-xl font-bold text-white shadow-xl shadow-blue-200 transition-transform hover:scale-105"
						>無料体験に申し込む ＞</button
					>
					<!-- <p class="text-xs font-medium text-slate-400">※中学生・小学生・高校生が対象です</p> -->
				</div>
			</div>
			<div class="relative mt-auto mb-16 flex flex-1">
				<!-- 画像プレースホルダー: がくなび.png のヒーロー画像に相当 -->
				<!-- <div
					class="aspect-4/3 w-full overflow-hidden rounded-3xl border-8 border-white bg-slate-200 shadow-2xl lg:aspect-video"
				>
					<img
						src="/images/hero.webp"
						alt="がくなびの活動風景"
						class="h-full w-full object-cover"
					/>
				</div> -->
				<div
					class="absolute -right-6 -bottom-7 mt-auto -rotate-6 transform rounded-2xl bg-accent px-6 py-4 font-black text-blue-900 italic shadow-lg"
				>
					キミの「やってみたい！」がきっと見つかる！ ✨
				</div>
			</div>
		</div>
	</section>

	<!-- About Section -->
	<section id="about" class="bg-blue-50 px-6 pt-28 pb-24">
		<div class="mx-auto max-w-7xl">
			<div class="flex flex-col items-center gap-12 lg:flex-row">
				<div class="flex-1 space-y-6">
					<h3 class="text-4xl leading-tight font-black text-blue-900 italic">
						がくなびで広がる学びの世界
					</h3>
					<div class="space-y-4 text-lg leading-relaxed text-slate-600">
						<p>
							これまでの学習は、知識を詰め込む「インプット」が中心でした。
							しかし、これからの時代に本当に必要なのは、その知識を使って何を生み出せるかという「アウトプット」の力です。
						</p>
						<p>
							がくなびは、最新のAIを「魔法の道具」のように使いこなし、キミの「好き」や「興味」を形にするプロジェクト学習の場所です。
							学校でも塾でもない、キミが主役になれる新しい放課後を体験しましょう。
						</p>
					</div>
				</div>
				<div class="grid flex-1 grid-cols-1 gap-6 md:grid-cols-2">
					<div
						class="rounded-3xl border border-yellow-100 bg-accent p-8 shadow-sm transition-transform hover:scale-105"
					>
						<span class="mb-4 block text-3xl">🚀</span>
						<h4 class="mb-2 text-xl font-bold text-blue-900">AIは最高の相棒</h4>
						<p class="text-sm leading-relaxed text-slate-500">
							難しい技術はAIに任せてOK。キミの「アイデア」を最優先に形にします。
						</p>
					</div>
					<div
						class="rounded-3xl border border-yellow-100 bg-accent p-8 shadow-sm transition-transform hover:scale-105"
					>
						<span class="mb-4 block text-3xl">🛡️</span>
						<h4 class="mb-2 text-xl font-bold text-blue-900">自分だけのサードプレイス</h4>
						<p class="text-sm leading-relaxed text-slate-500">
							学校が物足りなくても大丈夫。ありのままのキミが輝ける場所です。
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Workshops Section -->
	<section id="workshops" class="px-6 py-24 text-center">
		<h3 class="mb-16 text-3xl font-black text-slate-800 italic">
			学べるコース<span class="text-blue-600">。</span>
		</h3>
		<div class="mx-auto grid max-w-7xl grid-cols-1 gap-4 md:grid-cols-3 lg:grid-cols-6">
			<!-- Workshop Card -->
			{#each workshops as ws (ws.title)}
				<div
					class="reveal-on-scroll group rounded-3xl border border-slate-100 bg-white p-1 text-left shadow-sm transition-all hover:-translate-y-2 hover:shadow-xl"
				>
					<div class="flex items-center justify-center">
						<div class="mb-4 text-4xl">{ws.icon}</div>
						<h4 class="mb-2 text-xl font-bold text-blue-900">{ws.title}</h4>
					</div>

					<p class="mb-2 px-4 text-sm leading-relaxed text-slate-500">{ws.desc}</p>
					<div class="aspect-video overflow-hidden rounded-xl bg-slate-100">
						<img
							src={ws.image}
							alt={ws.title}
							class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-110"
						/>
					</div>
				</div>
			{/each}
		</div>
	</section>

	<!-- Teamwork Section -->
	<section class="overflow-hidden bg-blue-50 px-6 py-24">
		<div class="mx-auto flex max-w-7xl flex-col items-center gap-16 lg:flex-row">
			<div class="flex-1 space-y-6">
				<h3 class="text-3xl leading-tight font-black text-blue-900">
					繋がる学びが<br />やる気を育てる。
				</h3>
				<p class="leading-relaxed text-slate-600">
					全国どこからでも参加できるオンライン授業。<br />
					質問や意見を気軽に共有できるから、<br />
					安心して授業を受けられます。
				</p>
				<!-- Chat Mockup -->
				<div class="space-y-3 pt-6">
					<div
						class="max-w-xs rounded-2xl rounded-bl-none border border-blue-100 bg-white p-3 text-sm shadow-sm"
					>
						<p class="mb-1 text-[10px] font-bold text-blue-600">ハルト 中2</p>
						<p>プロジェクトヘイルメアリーで読書感想文を書くのはありですか？👏</p>
					</div>
					<div
						class="ml-8 max-w-xs rounded-2xl rounded-bl-none border border-blue-100 bg-white p-3 text-sm shadow-sm"
					>
						<p class="mb-1 text-[10px] font-bold text-green-600">メンター さくら</p>
						<p>次はこのシーンを作ってみよう！</p>
					</div>
					<div
						class="ml-16 max-w-xs rounded-2xl rounded-bl-none border border-blue-100 bg-white p-3 text-sm shadow-sm"
					>
						<p class="mb-1 text-[10px] font-bold text-pink-600">ゆな 中３</p>
						<p>私がBGM付けてみるね！</p>
					</div>
				</div>
			</div>
			<div class="relative flex-1">
				<div
					class="aspect-video rotate-2 overflow-hidden rounded-[3rem] bg-slate-300 shadow-2xl transition-transform hover:rotate-0"
				>
					<img
						src="/images/team-photo.webp"
						alt="チームでの活動"
						class="h-full w-full object-cover"
					/>
				</div>
			</div>
		</div>
	</section>

	<!-- Steps Section -->
	<section id="steps" class="px-6 py-24 text-center">
		<h3 class="mb-16 text-3xl font-black text-slate-800 italic">学習の進め方</h3>
		<div class="relative mx-auto grid max-w-5xl grid-cols-1 gap-12 md:grid-cols-3">
			<div
				class="absolute top-1/2 right-[25%] left-[25%] -z-10 hidden h-1 -translate-y-1/2 bg-blue-100 md:block"
			></div>
			{#each steps as s (s.step)}
				<div class="relative rounded-3xl border border-blue-50 bg-white p-8 shadow-lg">
					<span
						class="absolute -top-4 left-6 rounded-full bg-primary px-3 py-1 text-xs font-black text-white"
						>{s.step}</span
					>
					<div class="mb-4 text-4xl">{s.icon}</div>
					<h4 class="mb-2 text-lg font-bold">{s.title}</h4>
					<p class="text-xs leading-relaxed text-slate-500">{s.desc}</p>
				</div>
			{/each}
		</div>
		<div class="pt-12 text-center text-2xl">
			自分のペースで学習することも、みんなと一緒に学習することも可能<br />
			同じ内容の授業を受け直すこともできるので安心
		</div>
	</section>

	<!-- Testimonials -->
	<section id="members" class="bg-slate-50 px-6 py-24">
		<h3 class="mb-16 text-center text-3xl font-black text-slate-800 italic">生徒たちの声</h3>
		<div class="mx-auto grid max-w-7xl grid-cols-1 gap-8 md:grid-cols-3">
			{#each members as member (member.name)}
				<div
					class="reveal-on-scroll flex items-center gap-6 rounded-3xl border border-slate-100 bg-white p-8 shadow-sm"
				>
					<div
						class="h-32 w-32 shrink-0 overflow-hidden rounded-full border-2 border-white bg-slate-200 shadow-sm"
					>
						<img src={member.avatar} alt={member.name} class="h-full w-full object-cover" />
					</div>
					<div>
						<p class="mb-1 text-sm leading-snug font-bold text-slate-800">{member.comment}</p>
						<p class="text-xs text-slate-400">{member.grade} ・ {member.name}</p>
					</div>
				</div>
			{/each}
		</div>
	</section>

	<!-- Final CTA -->
	<section class="final relative overflow-hidden p-10">
		<div class="absolute inset-0"></div>
		<div class="relative z-10 space-y-8">
			<h3 class="text-4xl font-black italic lg:text-5xl">さあ、いっしょに未来をつくろう。</h3>
			<p class="text-xl font-bold">
				がくなびで、あなたの「好き」や「得意」を見つけて、<br />
				可能性を広げていこう！
			</p>

			<button
				class="rounded-full bg-primary px-16 py-6 text-2xl font-black text-white shadow-2xl transition-all hover:scale-105"
			>
				無料体験に申し込む ＞
			</button>
			<p class="text-xl font-bold">まずは無料で体験！ ＼ 顔出しなし（カメラオフ）でも参加OK ／</p>
		</div>
	</section>

	<!-- Footer -->
	<footer class="footer border-t border-slate-100 bg-white px-6 py-16 text-center">
		<div class="mx-auto flex max-w-7xl flex-col items-center justify-between gap-12 md:flex-row">
			<div class="flex items-center gap-2">
				<img src="/images/favicon.png" alt="logo" class="h-12 rounded-2xl" />
				<span class="text-lg font-bold tracking-tight text-blue-900">がくなび</span>
			</div>
			<nav
				class="flex flex-wrap justify-center gap-x-8 gap-y-4 text-xs font-bold tracking-widest text-slate-500 uppercase"
			>
				<a href="#about" class="hover:text-primary">がくなびについて</a>
				<a href="#workshops" class="hover:text-primary">学べるコース</a>
				<a href="#steps" class="hover:text-primary">学習の進め方</a>
				<a href="#members" class="hover:text-primary">ギルドメンバー</a>
				<a href="#faq" class="hover:text-primary">よくある質問</a>
				<a href="#contact" class="hover:text-blue-600">お問い合わせ</a>
			</nav>
			<div class="flex gap-4">
				<div
					class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full bg-slate-100 text-slate-400 transition-colors hover:bg-blue-50 hover:text-blue-600"
				>
					𝕏
				</div>
				<div
					class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full bg-slate-100 text-slate-400 transition-colors hover:bg-pink-50 hover:text-pink-600"
				>
					📸
				</div>
				<div
					class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full bg-slate-100 text-slate-400 transition-colors hover:bg-red-50 hover:text-red-600"
				>
					▶️
				</div>
				<div
					class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full bg-slate-100 text-slate-400 transition-colors hover:bg-indigo-50 hover:text-indigo-600"
				>
					💬
				</div>
			</div>
		</div>
		<p class="mt-12 text-[10px] text-slate-400">© がくなび All Rights Reserved.</p>
	</footer>
</div>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}

	.hero {
		background-image: url('/images/hero.webp');
		background-size: cover;
		background-position: right;
		background-repeat: no-repeat;
		clip-path: ellipse(150% 100% at 50% 0%);
		/* clip-path: url(#wave-clip); */
	}

	#about {
		margin-top: -3rem;
		background-image: url('/images/about.webp');
		background-size: cover;
		background-position: right;
		background-repeat: no-repeat;
	}

	.final {
		background-image: url('/images/footer.webp');
		background-size: cover;
	}

	/* 1. アニメーション（キーフレーム）の定義 */
	@keyframes fadeInUp {
		from {
			opacity: 0;
			transform: translateX(100px) scale(0.8);
		}
		to {
			opacity: 1;
			transform: translateX(0) scale(1);
		}
	}
	/* 2. アニメーションを適用するクラス */
	.reveal-on-scroll {
		/* 互換性のためのフォールバック（未対応ブラウザでは最初から表示されるようにする） */
		opacity: 1;
		/* スクロール駆動アニメーションに対応しているブラウザのみに適用 */
		@supports (animation-timeline: view()) {
			animation: fadeInUp linear both;

			/* スクロール量（ビューポートとの交差）をアニメーションのタイムラインにする */
			animation-timeline: view();

			/* アニメーションを開始・終了するタイミングの調整 */
			/* entry 10% (画面の下端に入り始めた時) から cover 30% までに完了 */
			animation-range: entry 20% cover 30%;
		}
	}
</style>
