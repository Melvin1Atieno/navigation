# Circular navigation


## One

### Content.

1. Div containing navigation Items.
2. An overlay to cover page when the navigation is open
3. A button to trigger opening and closing of the navigation bar.

### Logic

1. Determine central angle size for each navigation item.
        To distribute the items on a semi-circle.
            central angle : **180deg/5 = 36deg**
        To distriute the items in the whole circle
            central angle : **360deg/6*=72deg**
2. To create the central angle?
[skew() css function](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/skew)

        90deg - xdeg where x is the central angle value

    **note**
        content inside the list items will also be skewed on that case we will have to unskew the anchors inside each item.

### Steps
1. Position the items absolutely inside their container.

2. Set the transform-origin for each item to be the bottom right corner.

3. Translate the items up and to the left just enough so that their transform origin coincides with the containers center.

4. Rotate the list items clockwise into position by: angle y= i * x(where i=index of the item which starts at zero, and x=value of central angle as shown in the logic area)


5. Skew them to get the central angle :smirk: