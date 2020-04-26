#Art

Collection of computational art (idk if that's a term).

There are two main notebooks in here:

1. Style Transfer: A Colab notebook about neural style transfer (adapted from the Pytorch tutorial)
2. PolyArt Generator: An algorithm to convert an image into PolyArt (insported by my friend Varun's profile pic). My current/past attempts are listed:
	* Randomly draw points from the picture, create a list of polygons that cover the picture by grouping each point with its k nearest neghbors (ideally triangles), and replace each pixel within each polygon with the mean color within each polygon 
		* This worked moderately well, the problem is that it doesn't cover the entire picture (see trial1.png).
		* Another issue is that it would be better to have more polygons where there is more details int he picure (for example eyes would have more polygons than cheeks). This can be solved by using contours or canny edge detection as a way to generate points
	* Uniformly draw every x point,create a list of polyons that cover the picture by grouping each point with its k nearest neighbors, and replace each pixel within each polygon with the mean color within each polygon 
		* This kinda works, but there is still the issue of not covering the entire area. I prefer the more random initilization of points.
	* (Yet to be implemented) Create a polygon from contours detected from canny edge detection (convex hull of the points returned), run a polygon triangularization algorithm on the returned convex hull (need to look into the links listed below more)
		* https://en.wikipedia.org/wiki/Polygon_triangulation
		* https://people.csail.mit.edu/indyk/6.838-old/handouts/lec4.pdf
		* https://www.geeksforgeeks.org/minimum-cost-polygon-triangulation/


