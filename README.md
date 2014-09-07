TextSet
=======


TextSet Class for JanusVR

cahorton 2014-09-07

A TextSet is a collection of lines (text objects) organized so they look like a paragraph

Create a TextSet with optional parameters, and then use addLine to add text

    room.tSet = new TextSet();
    room.tSet.addLine("Your Pizza Order Status: Pending");
    room.tSet.addLine("Sausage");
    room.tSet.addLine("Mushrooms");

Text will wrap at the specified number of columns (default 40)

Optional TextSet parameters are columns, spacing, and justification

    room.tSet = new TextSet(60, 3, 2);  // 60 columns, triple spaced, right justified

* Columns: default is 40
* Spacing: 1 = single spaced, 2 = double spaced, etc.  Default is 2 for readability
* Justification: 0 = left, 1 = center, 2 = right.  Default is left


To update a specific line, use addLine but pass in a line number e.g. 

    addLine("Your Pizza Order Status: In the Oven", 0);
    

To insert a line use insertLine

    insertLine("Extra Cheese",1);
    
Both addLine and insertLine can also take a color vector as an optional 3rd argument 

Individual line positions, rotations, and scales are set automatically based on the parent TextSet values
and should not be manipulated individually.

To manipulate the TextSet after it is created, use:
* setPos(Vector3)  - default is (0,0,0)
* setFwd(Vector3)  - default is (0,0,1)
* setScale(number) - default is 2
* setCol(Vector3)  - default is blue (0,0,1)

Examples:

    room.tSet.setPos(Vector(0,3,-10); // move
    room.tSet.setScale(4);            // scale up
    room.tSet.setFwd(Vector(1,0,1));  // change orientation, note y is ignored
    room.tSet.setCol(Vector(1,0,0));  // red
    



