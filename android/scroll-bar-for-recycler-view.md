In order to use scrollbars to control `RecyclerView`'s scroll position,we need use `fastScrollEnabled` property.In addition,don't forget to set the track/thumb drawable for both vertical and horizontal directions,or it will crash.

Sample code:
```xml
<androidx.recyclerview.widget.RecyclerView
    android:id="@+id/recycler_view"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fastScrollEnabled="true"
    android:scrollbars="none"
    android:scrollbarThumbVertical="@drawable/scrollbar_thumb"
    android:scrollbarTrackVertical="@drawable/scrollbar_track"
    android:scrollbarThumbHorizontal="@drawable/scrollbar_thumb"
    android:scrollbarTrackHorizontal="@drawable/scrollbar_track"
    app:layoutManager="androidx.recyclerview.widget.LinearLayoutManager"
    />
```
Becasue the default `View`'s scrollbar can't control scroll position,we need disable it by using 
```xml
android:scrollbars="none"
```

If you don't see the scrollbar,try to set transparent background color for the RecyclerView.
```xml
android:background="@android:color/transparent"
```
