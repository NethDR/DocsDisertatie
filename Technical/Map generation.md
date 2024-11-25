
# Possible algorithms

See [this guide](https://www.cs.cmu.edu/~112-n23/notes/student-tp-guides/Terrain.pdf) from Carnegie Mellon University's Fundamentals of Programming and Computer Science course.

[Diamond-square algorithm](https://en.wikipedia.org/wiki/Diamond-square_algorithm) (Implemented in Unity as demo)
[Perlin noise terrain generation](https://adrianb.io/2014/08/09/perlinnoise.html)
[Voronoi noise](https://www.ronja-tutorials.com/post/028-voronoi-noise/)

## Main Idea

Perhaps a graph-based approach could work.

Generate a graph of areas for a player's "side" of the map, then connect 1 copy of it for each player, then randomly disperse the nodes in a fair manner. Finally use other algorithms such as the Voronoi noise one to generate the map.

![](/Imgs/PlayerSideGraph.png)

Example of a possible graph for the side of a player, depicting half of the StarCraft 2 Ladder map [Alcyone](https://sc2arcade.com/map/2/249431/).

![](/Imgs/FullMapGraph.png)

Extension of previous graph for 2 players, the full Alcyone map.

![](/Imgs/3Player_.png)

Possible layout for a "3 Player Alcyone"


Graph generation could be based on (Delaunay triangulation)[https://en.wikipedia.org/wiki/Delaunay_triangulation]