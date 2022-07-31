<script>
	const genreData = [
		['장르 1', 12345, 1234567890, 12345, 12345678, 12345, 12345678, 12345],
		['장르 2', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 3', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 4', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 5', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 6', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 7', 12345, 12345, 12345, 12345, 12345, 12345, 12345],
		['장르 8', 12345, 12345, 12345, 12345, 12345, 12345, 12345]
	];
</script>

<div class="container px-3 py-2.5 mt-6">
	<div>
		<span class="text-3xl font-light dark:text-gray-200">장르별 통계</span>
	</div>
	<table class="mt-3 w-full table-auto font-light dark:text-gray-200">
		<thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
			<tr class="text-left">
				<th class="p-3 font-normal">장르</th>
                <th class="p-3 font-normal">작품수</th>
                <th class="p-3 font-normal">조회수</th>
                <th class="p-3 font-normal">평균 조회수</th>
                <th class="p-3 font-normal">좋아요 수</th>
                <th class="p-3 font-normal">평균 좋아요 수</th>
                <th class="p-3 font-normal">선작수</th>
                <th class="p-3 font-normal">평균 선작 수</th>
			</tr>
		</thead>
		<tbody>
			{#each genreData as keyword}
				<tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
					{#each keyword as data}
						<td class="p-3">{data.toLocaleString()}</td>
					{/each}
				</tr>
			{/each}
		</tbody>
	</table>
</div>
