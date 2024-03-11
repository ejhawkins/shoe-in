<script lang="ts">
  import WidgetStaticText from '$lib/components/Widgets/WidgetStaticText.svelte';
	import WidgetUserInput from '$lib/components/Widgets/WidgetUserInput.svelte';
	import WidgetTextGeneration from '$lib/components/Widgets/WidgetTextGeneration.svelte';
	import WidgetImageGeneration from '$lib/components/Widgets/WidgetImageGeneration.svelte';

  import { AppState } from '$lib/stores/appv2.svelte';
	import WidgetChatbot from '$lib/components/Widgets/WidgetChatbot.svelte';

  const appTitle = $AppState.appDetails.title;
  const appAuthor = $AppState.appDetails.author;
  const appUrl = $AppState.appDetails.url;


  const updateWidgetValue = (index: number, newValue: any) => {
    $AppState.widgets[index].value = newValue;
  }
</script>

<svelte:head>
  <title>{appTitle}</title>
</svelte:head>
<!--- Navbar -->
<nav class="navbar party-header">
  <div class="container-fluid">
    <div class="col-10 col-sm-6"><div class="logo"></div></div>
    <div class="col-2"> <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button></div>
    <div class="navbar-collapse collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#prompt-stylist">AI Fashion Styling</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#playlist">Playlist</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#moody">Moodboard</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#color-your-mood">Color Your Mood</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#style-goals">Style Goals</a>
        </li>
       
       
      </ul>
    </div>
  </div>
</nav>


<main class="party-body container-lg container-xl container-xxl">
  <!-- Hero -->
  <div class="hero d-sm-none"></div>
  <div class="hero-tablet"></div>
  <!--- User Information-->
  <div id="username" class="col-12">
      <p id="name">Good Morning, Erica,</p>
      <p>IT’s Monday, 3/11/2024 at 8:00PM</p>
      <p><span style="float: left;">Douglasville, GA</span> <img src="https://d3baq5jflnwbxj.cloudfront.net/cloud.png" width="30px" style="float: left;padding-left: 10px;"></p>
      <br>
      <br>
      <p id="quote"> <img src="https://d3baq5jflnwbxj.cloudfront.net/sparkle.png" width="30px" style="float: left;padding-left: 10px;"><span style="float: left;">Quote of the Day:</span></p>
      <br>
      <p>“FOllow your dreams”
       <br> - ERica</p>
      <p id="style-me"><a class="nav-link" aria-current="page" href="#prompt-stylist"><img src="https://d3baq5jflnwbxj.cloudfront.net/play-button.png" style="width: 50px;"></a></p>
      <br>
      <img id="sm" src="https://d3baq5jflnwbxj.cloudfront.net/ready.png" style="margin:auto">
      <br>
  </div>
  
   

  <div id="playlist" style="padding-bottom: 25px;" class="col-12">
    <h3>Playlists</h3>
    <div class="accordion" id="accordionPanelsStayOpenExample">
      <div class="accordion-item">
        <h2 class="accordion-header" id="panelsStayOpen-headingOne">
          <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseOne" aria-expanded="true" aria-controls="panelsStayOpen-collapseOne">
            WOMEN'S HERSTORY VOCALS
          </button>
        </h2>
        <div id="panelsStayOpen-collapseOne" class="accordion-collapse collapse show" aria-labelledby="panelsStayOpen-headingOne">
          <div class="accordion-body">
            <img src="https://d3baq5jflnwbxj.cloudfront.net/herstory.png" style="margin: auto;">
            Breaking the glass ceiling for better wages for women, for more equality check out this playlist. Featuring Ariana Grande.
          </div>
        </div>
      </div>
      <div class="accordion-item">
        <h2 class="accordion-header" id="panelsStayOpen-headingTwo">
          <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseTwo" aria-expanded="false" aria-controls="panelsStayOpen-collapseTwo">
            party rock hackathon jams
          </button>
        </h2>
        <div id="panelsStayOpen-collapseTwo" class="accordion-collapse collapse" aria-labelledby="panelsStayOpen-headingTwo">
          <div class="accordion-body">
            <strong>This is the second item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
          </div>
        </div>
      </div>
      <div class="accordion-item">
        <h2 class="accordion-header" id="panelsStayOpen-headingThree">
          <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panelsStayOpen-collapseThree" aria-expanded="false" aria-controls="panelsStayOpen-collapseThree">
            ready for office creative boost
          </button>
        </h2>
        <div id="panelsStayOpen-collapseThree" class="accordion-collapse collapse" aria-labelledby="panelsStayOpen-headingThree">
          <div class="accordion-body">
            <strong>This is the third item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="ad"><img src="https://d3baq5jflnwbxj.cloudfront.net/macys.png" style="margin: auto;"><p>Our goal is to serve the less visible community of the less fortunate, are you making less than $25 and hour? Apply for a business suit grant or use our exclusive promotions once you've found a style that fits your taste. </p></div>
  <br>
  <br>
  <h3 style="width:100%;">Style Mood Board</h3>
  <div id="moody" style="background-color: black; height: 100vh;width: 100%;margin-top:10px;">
      <h3>upload your inspiration and looks</h3>
      <div class="col-12" style="background-color: white;    width: 90%;
      height: 92vh;
      margin: auto;
      margin-top: 13px; text-align: center;">
    
      <input
      type="file"
      id="fileElem"
      multiple
      accept="image/*"
      style="display:none" />
    <a href="#" id="fileSelect">Select some files</a>
    <div id="fileList">
      <p>No files selected!</p>
    </div>
    <script>
      const fileSelect = document.getElementById("fileSelect"),
      fileElem = document.getElementById("fileElem"),
      fileList = document.getElementById("fileList");
  
      fileSelect.addEventListener(
        "click",
        (e) => {
          if (fileElem) {
            fileElem.click();
          }
          e.preventDefault(); // prevent navigation to "#"
        },
        false,
      );
  
      fileElem.addEventListener("change", handleFiles, false);
  
      function handleFiles() {
        if (!this.files.length) {
          fileList.innerHTML = "<p>No files selected!</p>";
        } else {
          fileList.innerHTML = "";
          const list = document.createElement("div");
          fileList.appendChild(list);
          for (let i = 0; i < this.files.length; i++) {
            const li = document.createElement("div");
            list.appendChild(li);
  
            const img = document.createElement("img");
            img.src = URL.createObjectURL(this.files[i]);
            img.height = 60;
            img.onload = () => {
              URL.revokeObjectURL(img.src);
            };
            li.classList.add("draggable");
            li.appendChild(img);
            const info = document.createElement("span");
            info.innerHTML = `${this.files[i].name}: ${this.files[i].size} bytes`;
            li.appendChild(info);
          }
        }
      }
  
     </script>
    </div>
  </div>
  <h3 style="width:100%;padding-top: 20px;">Style Bookmarks</h3>
  
  <div class="card" style="margin-bottom: 30px;">
    <div class="card-body" style="padding: 0px;width: 361px;">
      <div style="border-radius: 8px 0px 0px 8px;background-color: red;height: 201px;width: 166px;background-image: url('https://d3baq5jflnwbxj.cloudfront.net/harlm.png');float: left;"></div>
      <div style="float: left;vertical-align:top; width: 50%;padding: 10px;">Harlem  is a show to watch for style</div>
      <br>
      <p style="color: #B2AAAA;font-family: 'Red Hat Display';
      font-size: 10px;
      font-style: normal;
      font-weight: 600;
      line-height: normal;
      letter-spacing: -0.9px;
      text-transform: uppercase;"><span style=" display: inline-block;width: 25%;
      padding-left: 10px;"><img src="https://d3baq5jflnwbxj.cloudfront.net/url.png" style="width: 24%"></span><span style="width: 26%;margin-left: -55px;">www.amazon.com</span></p></div>
  </div>


  <div class="card" style="margin-bottom: 30px;">
    <div class="card-body" style="padding: 0px;width: 361px;">
      <div style="border-radius: 8px 0px 0px 8px;background-color: red;height: 201px;width: 166px;background-image: url('/src/lib/metgala.png');float: left;"></div>
      <div style="float: left;vertical-align:top; width: 50%;padding: 10px;">Met Gala</div>
      <br>
      <p style="color: #B2AAAA;font-family: 'Red Hat Display';
      font-size: 10px;
      font-style: normal;
      font-weight: 600;
      line-height: normal;
      letter-spacing: -0.9px;
      text-transform: uppercase;"><span style=" display: inline-block;width: 25%;
      padding-left: 10px;"><img src="https://d3baq5jflnwbxj.cloudfront.net/url.png" style="width: 24%"></span><span style="width: 26%;margin-left: -55px;">www.vogue.com</span></p></div>
  </div>
  

  <div class="card" style="margin-bottom: 30px;">
    <div class="card-body" style="padding: 0px;width: 361px;">
      <div style="border-radius: 8px 0px 0px 8px;background-color: red;height: 201px;width: 166px;background-image: url('/src/lib/nyfw.png');float: left;"></div>
      <div style="float: left;vertical-align:top; width: 50%;padding: 10px;">NYFW FASHION WEEK</div>
      <br>
      <p style="color: #B2AAAA;font-family: 'Red Hat Display';
      font-size: 10px;
      font-style: normal;
      font-weight: 600;
      line-height: normal;
      letter-spacing: -0.9px;
      text-transform: uppercase;"><span style=" display: inline-block;width: 25%;
      padding-left: 10px;"><img src="https://d3baq5jflnwbxj.cloudfront.net/url.png" style="width: 24%"></span><span style="width: 26%;margin-left: -55px;">www.amazon.com</span></p></div>
  </div>
  
  
  <div class="party-widget-list" id="prompt-stylist">
    {#each $AppState.widgets as widget, index}
      {#if widget.type == "static-text"}
        <WidgetStaticText title={ widget.title } />
      {:else if widget.type == "text-input"}
        <WidgetUserInput title={ widget.title } />
      {:else if widget.type == "inferred-text"}
        <WidgetTextGeneration title={ widget.title } />
      {:else if widget.type == "chat"}
        <WidgetChatbot title={ widget.title } />
      {:else if widget.type == "image"}
        <WidgetImageGeneration title={ widget.title } />
      {/if}
    {/each}
  </div>
  
  <div class="party-footer">
    Generated by GenStack<br />
    Originally built with <a href={ appUrl } target="_blank">PartyRock</a>
  </div>
</main>