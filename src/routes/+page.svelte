<script>
	import { goto, afterNavigate, beforeNavigate } from '$app/navigation';

	const handleClick = () => {
		goto('/profile');
	};
	beforeNavigate((navigation) => {
		console.log({ before: navigation });
	});
	afterNavigate((navigation) => {
		console.log({ after: navigation });
	});
</script>

<h1>Hello World</h1>

<button on:click={handleClick}>Profile page</button>
