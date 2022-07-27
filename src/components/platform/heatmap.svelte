<script>
    let heatmapData = {
        mostViews: 5000,
        mondayViews: [237, 4794, 3235, 4253, 1850, 1378, 4250, 2939, 3976, 4878, 2703, 4381, 238, 1074, 3088, 4431, 25, 3000, 689, 4156, 2724, 2512, 721, 3262],
        tuesdayViews: [3357, 85, 4347, 4004, 2069, 2949, 1712, 2047, 3063, 2470, 3279, 3048, 4330, 1770, 1474, 2906, 1746, 1609, 3466, 4216, 2241, 1537, 4562, 3460],
        wednesdayViews: [4441, 873, 2211, 3862, 2096, 4690, 3818, 4650, 4308, 4175, 1665, 2963, 1957, 4911, 1279, 1087, 1241, 2675, 4997, 3136, 520, 378, 2166, 975],
        thursdayViews: [1116, 4839, 4734, 2316, 1984, 785, 3566, 747, 4799, 1849, 264, 4580, 804, 3093, 4942, 583, 3826, 1549, 4837, 3422, 1208, 1057, 4351, 3870],
        fridayViews: [3760, 367, 4787, 4385, 3539, 778, 3488, 4533, 1573, 1333, 280, 1474, 1780, 2209, 4035, 3560, 1284, 379, 4942, 227, 4709, 2083, 1735, 4364],
        saturdayViews: [470, 4242, 3499, 4039, 3924, 3184, 3160, 4889, 3375, 664, 3573, 1184, 3634, 4504, 2550, 2219, 2252, 2654, 3274, 4747, 2999, 2615, 719, 2033],
        sundayViews: [3668, 4351, 3970, 2272, 2988, 1717, 3469, 1618, 2024, 3692, 4493, 1360, 66, 3377, 4908, 3118, 579, 618, 2405, 585, 4165, 645, 1374, 108],
    }
</script>

<div class="container px-3 mt-4 py-2.5">
    <div class="flex flex-col gap-1.5">
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">월</span>
            {#each heatmapData.mondayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">화</span>
            {#each heatmapData.tuesdayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">수</span>
            {#each heatmapData.wednesdayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">목</span>
            {#each heatmapData.thursdayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">금</span>
            {#each heatmapData.fridayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">토</span>
            {#each heatmapData.saturdayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
        <div class="flex gap-1.5">
            <span class="mr-2 text-xl font-light dark:text-gray-200">일</span>
            {#each heatmapData.sundayViews as views}
                <div class="w-7 h-7 rounded-md" style="background-color: hsl(100, {views/heatmapData.mostViews*100}%, 50%);"></div>
            {/each}
        </div>
    </div>
</div>