<script>
    import {Tooltip} from 'flowbite-svelte'

    const heatmapData = {
        views: {
            mondayViews: [237, 4794, 3235, 4253, 1850, 1378, 4250, 2939, 3976, 4878, 2703, 4381, 238, 1074, 3088, 4431, 25, 3000, 689, 4156, 2724, 2512, 721, 3262],
            tuesdayViews: [3357, 85, 4347, 4004, 2069, 2949, 1712, 2047, 3063, 2470, 3279, 3048, 4330, 1770, 1474, 2906, 1746, 1609, 3466, 4216, 2241, 1537, 4562, 3460],
            wednesdayViews: [4441, 873, 2211, 3862, 2096, 4690, 3818, 4650, 4308, 4175, 1665, 2963, 1957, 4911, 1279, 1087, 1241, 2675, 4997, 3136, 520, 378, 2166, 975],
            thursdayViews: [1116, 4839, 4734, 2316, 1984, 785, 3566, 747, 4799, 1849, 264, 4580, 804, 3093, 4942, 583, 3826, 1549, 4837, 3422, 1208, 1057, 4351, 3870],
            fridayViews: [3760, 367, 4787, 4385, 3539, 778, 3488, 4533, 1573, 1333, 280, 1474, 1780, 2209, 4035, 3560, 1284, 379, 4942, 227, 4709, 2083, 1735, 4364],
            saturdayViews: [470, 4242, 3499, 4039, 3924, 3184, 3160, 4889, 3375, 664, 3573, 1184, 3634, 4504, 2550, 2219, 2252, 2654, 3274, 4747, 2999, 2615, 719, 2033],
            sundayViews: [3668, 4351, 3970, 2272, 2988, 1717, 3469, 1618, 2024, 3692, 4493, 1360, 66, 3377, 4908, 3118, 579, 618, 2405, 585, 4165, 645, 1374, 108],
            mostViews: 5000,
        },

        uploads: {
            mondayUploads: [11, 33, 46, 14, 64, 90, 66, 12, 79, 31, 57, 2, 13, 7, 8, 60, 12, 74, 77, 80, 41, 0, 51, 63],
            tuesdayUploads: [29, 84, 30, 100, 86, 63, 91, 7, 24, 47, 8, 53, 24, 15, 57, 90, 33, 14, 35, 25, 29, 8, 72, 81],
            wednesdayUploads: [59, 64, 7, 65, 33, 22, 50, 48, 56, 12, 12, 38, 23, 96, 56, 11, 0, 31, 41, 18, 24, 0, 60, 70],
            thursdayUploads: [81, 66, 56, 96, 8, 27, 57, 80, 61, 86, 0, 14, 77, 99, 15, 70, 80, 12, 60, 61, 32, 81, 90, 95],
            fridayUploads: [39, 87, 97, 6, 17, 12, 95, 60, 20, 79, 73, 47, 0, 91, 10, 16, 51, 88, 37, 52, 89, 88, 47, 91],
            saturdayUploads: [51, 79, 46, 29, 80, 68, 32, 56, 82, 88, 37, 30, 20, 0, 20, 95, 80, 52, 38, 18, 94, 50, 87, 31],
            sundayUploads: [82, 29, 32, 12, 34, 68, 81, 41, 8, 17, 32, 5, 95, 0, 61, 61, 89, 33, 31, 79, 76, 98, 56, 7],
            mostUploads: 100,
        },
    }

    const days = ["월", "화", "수", "목", "금", "토", "일"]
    const platformPricings = ["무료 작가연재", "무료 일반연재", "유료 연재작"]
    const platformGenres = ["무협", "판타지", "퓨전", "게임", "스포츠", "로맨스", "라이트노벨", "현대판타지", "대체역사", "전쟁·밀리터리", "SF", "추리", "공포·미스테리", "일반소설", "시·수필", "중·단편", "아동소설·동화", "드라마", "연극·시나리오", "BL", "팬픽·패러디"]

    let heatmapType, heatmapGenre, heatmapPricing;
</script>

<div class="container px-3 mt-8 py-2.5">
    <div>
        <span class="text-3xl font-light dark:text-gray-200">시간대별 {heatmapType} 통계</span>
    </div>
    <div>
        <span class="text-lg font-light text-gray-600 dark:text-gray-400">해당 시간에 업로드했을때 1시간동안 집계된 {heatmapType}</span>
    </div>

    <div class="flex mt-4">
        <select bind:value={heatmapType} id="underline_select" class="block py-1 px-0 w-1/6 text-sm text-gray-500 bg-transparent border-0 border-b-2 border-gray-200 appearance-none dark:text-gray-400 dark:border-gray-700 focus:outline-none focus:ring-0 focus:border-gray-200 peer">
            <option selected value="조회수">조회수</option>
            <option value="작품수">작품수</option>
        </select>
        {#if platformPricings.length > 0}
            <select bind:value={heatmapPricing} id="underline_select" class="ml-4 block py-1 px-0 w-1/6 text-sm text-gray-500 bg-transparent border-0 border-b-2 border-gray-200 appearance-none dark:text-gray-400 dark:border-gray-700 focus:outline-none focus:ring-0 focus:border-gray-200 peer">
                <option selected value="모든 연재">모든 연재</option>
                {#each platformPricings as pricing}
                    <option value={pricing}>{pricing}</option>
                {/each}
            </select>
        {/if}
        <select bind:value={heatmapGenre} id="underline_select" class="ml-4 block py-1 px-0 w-1/6 text-sm text-gray-500 bg-transparent border-0 border-b-2 border-gray-200 appearance-none dark:text-gray-400 dark:border-gray-700 focus:outline-none focus:ring-0 focus:border-gray-200 peer">
            <option selected value="모든 장르">모든 장르</option>
            {#each platformGenres as genre}
                <option value={genre}>{genre}</option>
            {/each}
        </select>
    </div>

    <div class="mt-3 flex flex-col gap-1.5">
        {#each days as day, dayIndex}
            <div class="flex gap-1.5">
                <span class="mr-2 text-xl font-light dark:text-gray-200">{day}</span>
                {#if heatmapType == "조회수"}
                    {#each Object.values(heatmapData.views)[dayIndex] as views, index}
                        <Tooltip class="whitespace-pre-line" content="{String(index).padStart(2, '0') + ":00 ~ " + String(index + 1).padStart(2, '0') + ":00\n"}조회수 : {views.toLocaleString() + '\n'}작품수 : {Object.values(heatmapData.uploads)[dayIndex][index].toLocaleString()}">
                            <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.views.mostViews*100}%, 50%);"></div>
                        </Tooltip>
                    {/each}
                {:else}
                    {#each Object.values(heatmapData.uploads)[dayIndex] as uploads, index}
                        <Tooltip class="whitespace-pre-line" content="{String(index).padStart(2, '0') + ":00 ~ " + String(index + 1).padStart(2, '0') + ":00\n"}작품수 : {uploads.toLocaleString() + '\n'}조회수 : {Object.values(heatmapData.views)[dayIndex][index].toLocaleString()}">
                            <div class="w-7 h-7 rounded-md" style="background-color: hsl(35, {uploads/heatmapData.uploads.mostUploads*100}%, 50%);"></div>
                        </Tooltip>
                    {/each}
                {/if}
            </div>
        {/each}
    </div>
</div>