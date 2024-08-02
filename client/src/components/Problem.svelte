<script>
  import { Card } from "flowbite-svelte";
  import { Rating, AdvancedRating, ScoreRating } from "flowbite-svelte";
  import { ArrowUpRightFromSquareOutline } from "flowbite-svelte-icons";

  export let title = "";
  export let difficulty = "";
  export let description = "";
  export let likes = 0;
  export let link = "#";

</script>

<Card>
  <h5
    class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
  >
    {title}
  </h5>
  <p class="mb-2"><strong>Difficulty:</strong>{difficulty}</p>
  <p class="text-gray-700 mb-4">{description}</p>
  <p><strong>Likes:</strong>{likes}</p>
  <a href="/" class="inline-flex items-center text-primary-600 hover:underline">
    View on LeetCode
    <ArrowUpRightFromSquareOutline class="w-4 h-4 ms-2.5" />
  </a>
</Card>


