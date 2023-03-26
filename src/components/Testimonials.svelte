<script>
	import { testimonials } from '../utils';
</script>

<section class="testimonials">
	<div class="section-title">
		<h1>Testimonials</h1>
	</div>
	<div class="section-body">
		<div class="section-left">left</div>
		<div class="section-right">right</div>
	</div>
	<div class="section-footer">circles</div>
</section>

<style>
	.section-body {
		display: flex;
		justify-content: space-around;
	}
	.section-footer {
		height: 80px;
		background-color: red;
	}
	.testimonials {
		height: 64rem;
	}
</style>
