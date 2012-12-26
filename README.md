CameraView
==========

This is a clone of Dino4674's Camera Viwe but I added the fucntion takePic() to take a picture

The original can be found at : https://github.com/Dino4674/CameraView

Usage is:



if (Ti.Media.isCameraSupported == true) {
  var imagePicker = require('ti.camera');
	camview2 = imagePicker.createView({
	    width : 320,
	    height : 320,
	    top:0,
	    left:0
	});
	camview.add(camview2);
	camview2.addEventListener("snapped", function(e) {
		Ti.API.debug("CALLBACK SNAPPED");
		Ti.API.debug(e);
    // e.media contains the snapped image
		snap = e.media; // this is just an example
		showImage(e.media); // again this is only an example 
	});
}

var b1 = Ti.UI.createButton({
  title : 'Take PIC'
});
var tapclick = function() {
	camview2.takePic();
};
b1.addEventListener('click',tapclick);
botview.add(b1);
