<video id="myVideo" width="400" controls>
    <source src="yourvideo.mp4" type="video/mp4">
</video>

<script>
const video = document.getElementById("myVideo");
const totalTime = 120; // 2 minutes
let startTime = Date.now();

video.play();

video.addEventListener("ended", function () {
    if ((Date.now() - startTime) / 1000 < totalTime) {
        video.currentTime = 0;
        video.play();
    }
});
</script>
