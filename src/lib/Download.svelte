<!-- Add icon library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<script lang="ts">
    let downloadMsg = "";
    let url = "README.md";
    let fileName = "README.md";

    async function download(){
        const anchorElement = document.createElement('a');
        anchorElement.href = url;
        anchorElement.download = fileName ?? '';
        anchorElement.click();
        anchorElement.remove();
        downloadMsg = "Downloaded the file!"
    }
</script>

<div>
    <div class="row">
        <button on:click={download} class="btn"><i class="fa fa-download"></i>
            Download
        </button>
    </div>
    <p class="pt-4 row">{downloadMsg}</p>
</div>