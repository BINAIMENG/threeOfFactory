# three.js

### Camera视角旋转
```
function myCameraTween(camera, angle, segs, during)
	{

	    var x = camera.position.x;
	    var y = camera.position.y;
	    var z = camera.position.z;


	    var endPosArray = new Array();

	    var perAngle = angle / segs;

	    for (var i = 1 ; i <= segs ; i++) {
	        var endPos = { "x": z * Math.sin(i * perAngle) + x * Math.cos(i * perAngle), "y": y, "z": z * Math.cos(i * perAngle) - x * Math.sin(i * perAngle) };

	        endPosArray.push(endPos);
	    }


	    var flag = 0;
        camera.position.x = endPosArray[flag].x;
        camera.position.y = endPosArray[flag].y;
        camera.position.z = endPosArray[flag].z;

        flag++;
	}
```

