A* (like Dijkstra) requires that all edge weights are non-negative

A* assumes that once a node is popped from the priority queue with the smallest f = g + h, its shortest path cost g is final

With a negative edge a later relaxation could produce a smaller g, violating the assumption

is it admissible? only if edge weights represent real geometric distances, or at least the true path cost is never smaller than the Euclidean distance (if the edge weights represent anything else, the euclidean distance may overestimate)

is it consistent? this is true when edge weights reflect actual geometric distances

$$
d(n, \text{goal}) = \sqrt{(x_n - x_g)^2 + (y_n - y_g)^2}
$$