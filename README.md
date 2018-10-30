# TPDragDropFramework
Drag/Drop framework for android to hold for long on screen on an object to drag it someother place
Android drag/drop framework allows your users to move data from one View to another View in the current layout using a graphical drag and drop gesture. As of API 11 drag and drop of view onto other views or view groups is supported.The framework includes following three important components to support drag & drop functionality −

**Drag event class.**

**Drag listeners.**

**Helper methods and classes.**

## Listening for Drag Event
If you want any of your views within a Layout should respond Drag event then your view either implements View.OnDragListener or setup onDragEvent(DragEvent) callback method. When the system calls the method or listener, it passes to them a DragEvent object explained above. You can have both a listener and a callback method for View object. If this occurs, the system first calls the listener and then defined callback as long as listener returns true.

The combination of the onDragEvent(DragEvent) method and View.OnDragListener is analogous to the combination of the onTouchEvent() and View.OnTouchListener used with touch events in old versions of Android.

## Starting a Drag Event
You start with creating a ClipData and ClipData.Item for the data being moved. As part of the ClipData object, supply metadata that is stored in a ClipDescription object within the ClipData. For a drag and drop operation that does not represent data movement, you may want to use null instead of an actual object.

Next either you can extend extend View.DragShadowBuilder to create a drag shadow for dragging the view or simply you can use View.DragShadowBuilder(View) to create a default drag shadow that's the same size as the View argument passed to it, with the touch point centered in the drag shadow.
