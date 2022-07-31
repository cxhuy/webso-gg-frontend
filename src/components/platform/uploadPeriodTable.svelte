<script>
    export let uploadPeriodData;
</script>

<div class="container px-3 py-2.5 mt-6">
    <div>
        <span class="text-3xl font-light dark:text-gray-200">연재 주기에 따른 통계</span>
    </div>
    <div class="hidden lg:block">
        <table class="mt-3 w-full table-auto font-light dark:text-gray-200">
            <thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
                <tr class="text-left">
                    <th class="p-3 font-normal">연재 주기</th>
                    <th class="p-3 font-normal">작품수</th>
                    <th class="p-3 font-normal">조회수</th>
                    <th class="p-3 font-normal">평균 조회수</th>
                    <th class="p-3 font-normal">좋아요 수</th>
                    <th class="p-3 font-normal">평균 좋아요 수</th>
                    <th class="p-3 font-normal">선작수</th>
                    <th class="p-3 font-normal">평균 선작수</th>
                </tr>
            </thead>
            <tbody>
                {#each uploadPeriodData as uploadPeriod}
                    <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                        {#each uploadPeriod as data}
                            <td class="p-3">{data.toLocaleString()}</td>
                        {/each}
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <div class="lg:hidden">
        {#each uploadPeriodData as uploadPeriod}
            <div class="mt-3 p-3 font-light rounded-md dark:text-gray-200 bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                <div class="text-xl">{uploadPeriod[0]}</div>
                <div class="mt-auto ml-auto">{uploadPeriod[1].toLocaleString()} 작품</div>
                <div class="mt-2 grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">조회수: </span>{uploadPeriod[2].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 조회수: </span>{uploadPeriod[3].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">좋아요 수: </span>{uploadPeriod[4].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 좋아요 수: </span>{uploadPeriod[5].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">선작수: </span>{uploadPeriod[6].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 선작수: </span>{uploadPeriod[7].toLocaleString()}</div>
                </div>
            </div>
        {/each}
    </div>
</div>
