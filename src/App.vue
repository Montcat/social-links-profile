<template>
	<main class="container">
		<div class="profile-container">
			<div class="description-container">
				<div class="img-container">
					<img :src="AvatarImage" alt="Avatar Image" class="profile-picture" />
				</div>
				<p class="name">Jessica Randall</p>
				<p class="location">London, United Kingdom</p>
				<p class="bio">"Front-end developer and avid reader."</p>
			</div>
			<ul class="links-container">
				<li class="link-items" v-for="item in listItems">
					<a href="#" class="link-item">
						{{ item }}
					</a>
				</li>
			</ul>
		</div>
	</main>

	<footer class="myFooter">
		<p>
			<span class="developer">Developer: </span
			><a href="https://github.com/Montcat" class="developer-link">Mont King</a>
		</p>
		<p>
			<span class="reference">Reference: </span
			><a
				href="https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ"
				>Frontend Mentor</a
			>
		</p>
	</footer>
</template>

<script setup>
	import { ref } from "vue";
	import AvatarImage from "@/assets/images/avatar-jessica.jpeg";

	const listItems = ref([
		"GitHub",
		"Frontend Mentor",
		"LinkedIn",
		"Twitter",
		"Instagram",
	]);
</script>

<style lang="scss" scoped>
	.container {
		display: grid;
		background-color: var(--ncl-off-black);
		padding: 5rem 0;
		height: 100%;

		.profile-container {
			margin: auto;
			display: grid;
			background-color: var(--ncl-dark-gray);
			width: 22rem;
			border-radius: 14px;
			padding: 2rem;

			.description-container {
				margin: auto;
				display: flex;
				flex-direction: column;

				.img-container {
					display: flex;
					align-items: center;
					justify-content: center;
					padding: 1rem;

					.profile-picture {
						height: 6rem;
						border-radius: 50%;
					}
				}

				.name {
					text-align: center;
					font-weight: 900;
					font-size: 1.5rem;
					padding-bottom: 0.5rem;
				}

				.location {
					text-align: center;
					color: var(--pcl-green);
					padding-bottom: 1.5rem;
					font-size: 0.9rem;
				}

				.bio {
					text-align: center;
					opacity: 0.7;
					font-size: 0.8rem;
					margin-bottom: 1rem;
				}
			}

			.links-container {
				list-style: none;
				padding: 0;
				margin: auto;
				display: grid;
				width: 100%;
				gap: 1rem;

				.link-item {
					margin: auto;
					width: 18rem;
					height: 2.5rem;
					border-radius: 8px;
					background-color: var(--ncl-gray);
					display: flex;
					justify-content: center;
					align-items: center;
					font-weight: 700;
					text-decoration: none;
					color: var(--ncl-white);
					transition: 0.5s;
				}

				.link-item:hover {
					background-color: var(--pcl-green);
					text-decoration: none;
					color: var(--ncl-off-black);
				}
			}
		}
	}

	.myFooter {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		padding: 20px 100px;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 2rem;

		p {
			color: var(--ncl-white);
			font-size: 18px;

			a {
				text-decoration: none;
				color: var(--pcl-green);
			}
		}
	}
</style>
