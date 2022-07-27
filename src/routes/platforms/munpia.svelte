<script>
    import PlatformInfo from "../../components/platform/platform-info.svelte";

    let platformInfoData = {
        platformName: "문파아",
        platformYear: 2012,
        platformMonth: 12,
        totalViews: 123456789,
        totalNovels: 1234,
        avgChapters: 123,
        avgPeriod: 1.2,
    }
</script>

<PlatformInfo platformInfoData={platformInfoData}/>