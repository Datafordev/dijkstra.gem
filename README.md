# Dijkstra's Algorithm 

[ ![Image](https://badge.fury.io/rb/dijkstra.svg "Image title") ](https://rubygems.org/gems/dijkstra "Badge")

Dijkstra's algorithm, conceived by computer scientist Edsger Dijkstra, is a graph search algorithm that solves in single-source
shortest path problem for a graph with non-negative edge path costs, producing a shortest path tree. 

![Screenshot](http://farm6.staticflickr.com/5572/15142640541_6ea1eb3d48.jpg)


## Install

```
gem install dijkstra 
```


## Usage

```

require 'dijkstra'

# In this context we have 9 edges or paths.
r = [[1, 2, 1],
     [1, 3, 9],
     [1, 5, 3],
     [2, 4, 3],
     [2, 3, 7],
     [4, 3, 2],
     [4, 1, 1],
     [5, 2, 4],
     [5, 4, 2]]

start_point = 1 # starting node
end_point = 3 # arrival node

ob = Dijkstra.new(start_point, end_point, r)

puts "Cost = #{ob.cost}"
puts "Shortest Path from #{start_point} to #{end_point} = #{ob.shortest_path}"

ob.write_to_file('shortestpath.out')

=>  shortestpath.out =>

    Cost -> 6
    Shortest Path -> [1, 2, 4, 3]

```

> You can use any kind of element as node, not only numbers.
> If returned cost is Infinity, and returned shortest_path is the starting node, then there is no Path that connects starting node and arrival node.

## Manual Installation

```

$ git clone git://github.com/oscartanner/dijkstra.gem.git
$ cd dijkstra.gem
$ gem build dijkstra.gemspec
$ gem install ./dijkstra-0.0.1.gem
$ ruby app.rb # testing
$ Cost = 6
$ Shortest Path  = [1,2,4,3]=> true

```


## References
  http://en.wikipedia.org/wiki/Dijkstra%27s_algorithm
