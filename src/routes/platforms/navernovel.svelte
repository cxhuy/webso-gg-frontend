<script>
    import PlatformInfo from "../../components/platform/platform-info.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";

    import NavernovelData from "../../jsondata/navernovel.json"
</script>

<PlatformInfo platformInfoData={NavernovelData.platformInfoData}/>
<Heatmap heatmapData={NavernovelData.heatmapData} platformPricings={NavernovelData.platformInfoData.platformPricings} platformGenres={NavernovelData.platformInfoData.platformGenres}/>
<GenreTable genreData={NavernovelData.genreData}/>
<UploadPeriodTable weeklyUploadCountData={NavernovelData.weeklyUploadCountData}/>
