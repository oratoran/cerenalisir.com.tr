<div class="w-screen h-screen">
    <iframe src="https://www.youtube.com/embed/Yj2iELI6OeI?controls=0&autoplay=1&mute=1" title="Explainatory Video"></iframe>
  </div>
  
  <div class="bg-black/50 absolute z-10 w-full h-full center flex justify-center items-center align-middle" id="text">
    <h1>Use a youtube video as a full screen background with CSS</h1>
  </div>
  
  <style>
  
  @import url("https://fonts.googleapis.com/css?family=Roboto:400,400i,700");
  
  body{
    overflow-x: hidden;
    font-family: Roboto, sans-serif;
  }
  
  h1{
    background: rgba(0,0,0,0.5);
    padding: 10px;
  }
  
  .video-container{
    width: 100vw;
    height: 100vh;
  }
  
   iframe {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100vw;
    height: 100vh;
    transform: translate(-50%, -50%);
  }
  
  #text{
    position: absolute;
    color: #FFFFFF;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  
  @media (min-aspect-ratio: 16/9) {
    .video-container iframe {
      height: 56.25vw;
    }
  }
  @media (max-aspect-ratio: 16/9) {
    .video-container iframe {
      width: 177.78vh;
    }
  }
  </style>