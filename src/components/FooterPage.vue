<template>
	<div class="footer">
		<img src="../assets/logo.svg"/>
		<div class="footer-contents">
			<div class="footer-elements">
				<a class="fa-solid fa-location-dot"></a>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
			</div>
			<div class="footer-elements-two">
				<div class="footer-elements-list" v-for="(footer, index) in footers" :key="index">
					<div class="footer-elements-items">
						<a :class="footer.icon"></a>
						<p>{{ footer.text }}</p>
					</div>
				</div>
			</div>
			<ul class="footer-list">
				<div>
					<a v-for="(item, index) in lists" :key="index">
						{{ item }}
					</a>
				</div>
				<a class="spacing"></a>
				<div>
					<a v-for="(item, index) in footerList" :key="index">
						{{ item }}
					</a>
				</div>
			</ul>
			<div class="social-icons">
				<a><i class="fa-brands fa-facebook-f"></i></a>
				<a><i class="fa-brands fa-twitter"></i></a>
				<a><i class="fa-brands fa-instagram"></i></a>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "FooterPage",
	data() {
		return {
			footers: [
	
				{
					icon: "fa-solid fa-phone-volume",
					text: "+1-543-123-4567",
				},
				{
					icon: "fa-solid fa-envelope",
					text: "example@fylo.com",
				},
			],
			lists: ["About Us", "Jobs", "Press", "Blog"],
			footerList: ["Contact Us", "Terms", "Privacy"],
			titles: ["lists", "footerList"],
		};
	},
};
</script>
