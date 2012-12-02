# Recursion Assignment

All the `POKEMAN` died in a fire last week, so we're going to try something different.

We're making a radical departure from your old realm of text-based assignments and making something fun and GRAPHICAL! Visual learners rejoice

## The Serpkinski Triangle
Many of you are familiar with the serpkinski triangle as a classic fractal (or doodle you do during math class).

A Serpkinski triangle is a classic form of recursion. To draw an example:

![Serpkinski Triangles][stri]

## Assignment

The goal of the assignment is quite simple: fill in the `drawSerp` function within the `Serpkinski` class to draw a Serpkinski triangle to the given order. The parameters are the `order` of the Serpkinski triangle, followed by the 3 coordinate pairs at which the triangle is to be drawn.

That is, if `drawSerp` is passed in with order `0`, you should draw a filled triangle, if it is initialized with order `1`, you should draw a triforce, and so on and so forth.

We have also given you a `drawTriangle` function you can use to draw on the canvas. It takes 6 parameters, which are the 3 (x,y) point pairs in order to draw the triangle.

### Hints
* You will probably want to call the `drawSerp` function from within the `drawSerp` function itself. But make sure you have a base case so that you don't recurse infinitely!
* The triangle we've given you isn't a perfect equailateral triangle. Don't worry -- it'll still work... but it means you'll have to do a little bit more math to figure out where to draw the inner triangels.
* Make sure you don't accidentally fill in the center triangle and only the corner triangles!
* This assignment is relatively easy, so if you find yourself writing too much code, you're probably wrong! Also, don't spoil the solution by asking someone or looking it up; it's really quite elegant

## Koch Snowflake

In celebration of last saturday's snow, we will also implement the Koch snowflake. To show:

![Koch Snowflake][ksno]

You'll need a little bit more math for this one, but we won't spoil the fun. In making errors you might end up with not quite a Koch snowflake, but nice looking.

We're making this one a little harder in that we've given you the scaffolding, but have not provided the necessary function signature for the recursion (although enterprising students might see a pattern w/ the Serpkinski example.

We've given you how to draw an equilateral triangle -- you can fill in the remaining section.

We _have_ however given you a `drawLine` function that takes in x1, y1, x2, y2 coordinates as parameters

## Tree Traversal

Hopefully you guys enjoyed the graphical examples! Now we sadly must depart from the realm of graphics, but we'll do an example that is infinitely more relevant to day-to-day computer science --- Tree traversal!

### In-Order Traversal
One of the most important recursive algorithms in computer science is being able to traverse through a tree in what we call via an "in-order" traversal. That is, given a tree of values, we wish to visit:

1. Visit left subnode
2. Print the root subnode
3. Visit right subnode

As an example, see the following:

![Tree In-Order Traversal][traversal]

This would print the following: 
    
    9, 12, 14, 17, 19, 23, 50, 54, 67, 72, 76
    
We call this in-order traversal because it is "in-order," that is, the way we read from left to right.

We have given you a tree-like structure and we wish for you to fill in the traversal function for the tree.

We have given you a very compact `Tree` class and `Node` class. The `Tree` class has only one member variable of the root node. The `Node` class contains the value of the node, and a pointer to the left node and the right node.  If there is no left or right node, then the value is `null` accordingly.

Fill in the function `inorderTraversal(Tree tree)` to recursively traverse through the tree and print the values of the nodes in-order.

We've given you an exampleTree that _should_ correspond to the tree in the given diagram (unless we were sleepy and typed it in wrong. In which case, tough luck. the world isn't always nice)

Hints:

* We havent given you _any_ scaffolding at all this time so you'll have to fill in all the pieces by yourself. You'll need to write helper functions in order traverse through the tree. For instance, you'll notice that the signature of the `inorderTraversal` function isn't even useful for recursion (because you can't recurse on the `Node` object. HINT HINT.
* Make sure to check for `null` values -- it means there is no child leave present


### Post-Order

Hopefully you were reading ahead, but if you weren't, this is an exercise in whether you made your code MODULAR. (an important principle of programming is to `don't repeat yourself`, or `DRY`)

Fill in the function `postorderTraversal(Tree tree)` to recursively traverse through the tree and print the values of the tree in post-order:

1. Visit the left subnode
2. Visit the right subnode
3. Print the root

To visualize this, we are essentially recursing as deep into the tree as possible before printing the given node. For the same example as tne in-order traversal, we would print:

    12, 14, 9, 19, 23, 17, 67, 72, 54, 76, 50

Once you have finished this, congrats! you're done!

## Addendum

Hopefully this is a welcome depature from the various text-based assignments.  Feel free to play around with the source and co-opt the code we've provided to draw your own things on the canvas.

Ask your nearby friendly instructor if you'd like to understand how anything works. Programming is much more than just the silly AP exam -- it gives you the power to create anything you want, whether they be pretty picture or even games!

[stri]: http://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Sierpinski_triangle_evolution.svg/680px-Sierpinski_triangle_evolution.svg.png
[ksno]: 
http://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/KochFlake.svg/362px-KochFlake.svg.png
[traversal]: http://2.bp.blogspot.com/_kRev2kjeMro/S4gCxNWfEVI/AAAAAAAACH4/-m8QszH_SmQ/s320/In+order+Traversal.png