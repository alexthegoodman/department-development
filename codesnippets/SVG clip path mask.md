# SVG clip path mask

**Animated animating icons**
Web:
* [GitHub - airbnb/lottie-web: Render After Effects animations natively on Web, Android and iOS, and React Native. http://airbnb.io/lottie/](https://github.com/airbnb/lottie-web)
* https://theblog.adobe.com/export-svg-animations-for-the-web-with-snap-svg/
* -After Effects is good for animation, but Animate CC is intended for the Web, is Vector Based, and exports to Snap.svg seem more lightweight-
	* On the other hand, I’d like to use the same tool for web and mobile
	* After Effects is actually great for vectors: https://www.youtube.com/watch?v=e_W-LlGrREg and Illustrator -> After Effects workflow, and Bodymovin / Lottie should animated the SVG without being heavy
	* Animate CC is okay, but the UI is a pain to navigate and it has fewer nifty tools, plus Snap.SVG must be installed ahead of time
* After Effects
	* Open in Ilustrator
	* Make sure SVG layers are all separate
		* Click Group and “Release to Layers”
	* [How to Animate an Icon in After Effects - YouTube](https://www.youtube.com/watch?v=e_W-LlGrREg)
	* https://www.youtube.com/watch?v=XLPchE7DPQE
	* Import into After Effects, do some conversions in the video
		* Save AS PDF Compatible, Import as Composition - retain layers
		* [Getting started · Lottie](http://airbnb.io/lottie/web/getting-started.html)
		* https://github.com/airbnb/lottie-web
		* 
	* etc

**Creating Clip Path**
Creating SVGs in Sketch is good. Not best for creating the clip-path SVG element needed.

Use Illustrator for clip-path SVGs. Create it in Illustrator from scratch. Use object -> clipping mask -> make to transform a group of layers into the mask.

Use a rectangle, then curve the top. Yay!

Pull the <clippath> chunk out into a simpler SVG like:

**Convert:**
<svg id="Layer_1" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 501 106">
  <defs>
    <style>
      .cls-1 {
        fill: none;
      }

      .cls-2 {
        clip-path: url(clip-path);
      }

      .cls-3 {
        fill: fff;
        stroke: #000;
        stroke-miterlimit: 10;
      }
    </style>
    <clipPath id="clip-path" transform="translate(0.5 0.5)">
      <path class="cls-1" d="M0,105C46.6,15,500,0,500,0H0Z"/>
    </clipPath>
  </defs>
  <title>footerCurve</title>
  <g class="cls-2">
    <rect class="cls-3" x="0.5" y="0.5" width="500" height="105"/>
  </g>
  <path class="cls-3" d="M-28.33,205.67" transform="translate(0.5 0.5)"/>
</svg>

**TO:**
<svg height="0" style="position: absolute;">
  <defs>
    <clipPath id="footerCurve" transform="translate(0.5 0.5)">
      <path class="cls-1" d="M0,105C46.6,15,500,0,500,0H0Z" />
    </clipPath>
  </defs>
</svg>

#department/development/codesnippets