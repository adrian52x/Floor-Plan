<script>
  let scale = 1;

function zoomIn() {
  scale += 0.5;
}

function zoomOut() {
  scale -= 0.5;
}
</script>

<div class="floor-plan">

    <div class="no-data font-digits px-4 py-2 ml-80 rounded-md text-xl font-semibold bg-gray-200 w-fit"> No data

      <button on:click={zoomIn}>Zoom In</button>
      <button on:click={zoomOut}>Zoom Out</button>
      <svg style="border: 1px solid black;" width="500" height="500">
        <rect x="10" y="10" width="100" height="100" fill="red" stroke="black" stroke-width="2" style="transform:scale({scale})" />
      </svg>

    </div> 
    

</div>



<style>
    .floor-plan {
    position: relative;
    top: 50px;
    text-align: center;
      width: 1150px;
      height: 1250px;
      /* border: 1px solid black; */
}
.no-data {
    margin-left: 20%;
    margin-top: 20%
  }

</style>

