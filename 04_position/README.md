# Positioning

Notes from codeSTACKr's CSS position tutorial. You can watch the tutorial [here](https://www.youtube.com/watch?v=XrHMv_9LCfo).

## Static

Static positioning is the default positioning in CSS. Therefore, if we do not declare a position, it is static.

This position flows along with the HTML document flow. In this example we created two `div`s, which are block elements by default, so the first element we created (`class=child-box-1`) will be positioned at the top, and the second one (`class=child-box-2`) will be positioned after it.

![](static-1.png)

## Relative

Relative position is similary to static, but we can now change the `top`, `right`, `bottom`, and `left` attributes. For example, is we set the first box to have `top=100px`, it will move down 100px from its original position.

![](down-100.png)

If we now add `right=50px` it will move 50 pixes away from its right side original position.

![](right-50.png)

Now box 1 is overflowing both its sibling (box 2) and its parent (box).

## Absolute

Absolute positioning removes the element from the documents flow and positions itself in reference to a container. That container must have a position too, otherwise the child box will position itself in reference to the `html` element.

![](absolute.png)

The reason why the green box does not show in our page is that to it, the orange box does not exists. Therefore, from greens perspective, he is the first child of the container (it is there, but it's behind the orange box).

If we now set `child-box-1` to have `right: 0;`, it will move all the way to the right, since its reference position is the `html` element. We can not see `child-box-2`.

![](right-0.png)

Similarly, if we set its `left: 0;`, then it goes all the way to the left.

![](left-0.png)

Now we add `top: 100px;`, and `child-box-1` will remove itself 100 pixels from the top of the page.

![](top-100.px)

If we wanted the green box to be ontop of the orange box, we'd need to use the `z-index` property. But, keep in mind that `z-index` only works if the element has a position. Since we don't want it to be removed from the documents flow, we'll give it `postion: relative;`

``` css
.child-box-2 {
  width: 250px;
  height: 250px;
  background: #14a76c;
  position: relative;
  z-index: 1;
}
```

![](green-on-top.png)

Now, to make the orange box move inside its parent, we need to assign a position to the parent. To achieve this, we give the parent `position: relative;`. Now orange is still all the way to the left, but using its parent container as a reference.

``` css
.child-box-1 {
  position: absolute;
  left: 0;
  top: 100px;
  width: 250px;
  height: 250px;
  background: #ff652f;
}
```

![](par-rel-left-0.png)

If we change back orange so that now its right position it set to be 0 pixels, then it'll move all the way to the right-hand side of its parent.

``` css
.child-box-1 {
  position: absolute;
  right: 0;
  top: 100px;
  width: 250px;
  height: 250px;
  background: #ff652f;
}
```

![](par-rel-right-0.png)

## Fixed



