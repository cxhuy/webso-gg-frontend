<script>
    const keywordData = [
        ["키워드 1", 12345, 12345],
        ["키워드 2", 12345, 12345],
        ["키워드 3", 12345, 12345],
        ["키워드 4", 12345, 12345],
        ["키워드 5", 12345, 12345],
        ["키워드 6", 12345, 12345],
        ["키워드 7", 12345, 12345],
        ["키워드 8", 12345, 12345],
        ["키워드 9", 12345, 12345],
        ["키워드 10", 12345, 12345],
        ["키워드 11", 12345, 12345],
        ["키워드 12", 12345, 12345],
        ["키워드 13", 12345, 12345],
        ["키워드 14", 12345, 12345],
        ["키워드 15", 12345, 12345],
        ["키워드 16", 12345, 12345],
        ["키워드 17", 12345, 12345],
        ["키워드 18", 12345, 12345],
        ["키워드 19", 12345, 12345],
        ["키워드 20", 12345, 12345],
    ]

</script>

<div class="container px-3 py-2.5">
    <div class="grid md:grid-cols-2 gap-4">
        <div class="mt-6">
            <div>
                <span class="text-3xl font-light dark:text-gray-200">키워드별 통계</span>
            </div>
            <table class="mt-3 w-full table-auto font-light dark:text-gray-200">
                <thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
                    <tr class="text-left">
                        <th class="w-1/3 p-3 font-normal">키워드</th>
                        <th class="w-1/3 p-3 font-normal">작품수</th>
                        <th class="w-1/3 p-3 font-normal">평균 조회수</th>
                    </tr>
                </thead>
                <tbody>
                    {#each keywordData as keyword}
                        <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                            {#each keyword as data}
                                <td class="p-3">{data}</td>
                            {/each}
                        </tr>
                    {/each}
                </tbody>
            </table>
        </div>
    </div>
</div>
