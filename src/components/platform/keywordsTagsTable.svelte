<script>
    export let keywordsTagsData
</script>

<div class="container px-3 py-2.5 mt-6">
    <div class="{keywordsTagsData.tagData.length > 0 ? "grid md:grid-cols-2 gap-4" : ""}">
        <div>
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
                    {#each keywordsTagsData.keywordData as keyword}
                        <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                            {#each keyword as data}
                                <td class="p-3">{data.toLocaleString()}</td>
                            {/each}
                        </tr>
                    {/each}
                </tbody>
            </table>
        </div>
        <div>
            <div>
                <span class="text-3xl font-light dark:text-gray-200">태그별 통계</span>
            </div>
            <table class="mt-3 w-full table-auto font-light dark:text-gray-200">
                <thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
                    <tr class="text-left">
                        <th class="w-1/3 p-3 font-normal">태그</th>
                        <th class="w-1/3 p-3 font-normal">작품수</th>
                        <th class="w-1/3 p-3 font-normal">평균 조회수</th>
                    </tr>
                </thead>
                <tbody>
                    {#each keywordsTagsData.tagData as tag}
                        <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                            {#each tag as data}
                                <td class="p-3">{data.toLocaleString()}</td>
                            {/each}
                        </tr>
                    {/each}
                </tbody>
            </table>
        </div>
    </div>
</div>
