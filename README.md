# Navigation menu with expandable list items

Sample android app for navigation menu with expandable list items in material design.

![Screenshot](https://github.com/D8thReaper/android-navigation-menu-expandable/blob/master/screen.jpg)


# Features

- Implemented using material design
- Easy to use
- Uses an expandable list view


# Working

## Layout 
Add a toolbar in your layout.

	<android.support.v7.widget.Toolbar 
		xmlns:android="http://schemas.android.com/apk/res/android"
    	xmlns:local="http://schemas.android.com/apk/res-auto"
    	android:id="@+id/toolbar"
    	android:layout_width="match_parent"
    	android:layout_height="wrap_content"
    	android:minHeight="?attr/actionBarSize"
    	android:background="?attr/colorPrimary"
    	local:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
    	local:popupTheme="@style/ThemeOverlay.AppCompat.Light" />	

Use a normal ExpandableListView in your drawer layout.

	<ExpandableListView
		android:id="@+id/left_drawer"
		android:layout_width="240dp"
    	android:layout_height="match_parent"
		android:layout_gravity="start"
		android:dividerHeight="1dp"
        android:divider="@color/list_divider"
		android:listSelector="@drawable/list_selector"
		android:background="@color/list_background" /> 
 
## Adapter for expandable list view

Make a new class with BaseExpandableListAdapter

	public class NavAdapter extends BaseExpandableListAdapter{

## Attach the drawerList to ActionBarDrawerToggle object

	actionBarDrawerToggle = new ActionBarDrawerToggle(this,drawer,toolbar,R.string.drawer_open,R.string.drawer_close )
   

# Acknowledgments


- [Ayush Pahwa](github.com/D8thReaper)
- [AndroidHive introduction to material design](http://www.androidhive.info/2015/04/android-getting-started-with-material-design/) for developing with material design
- [PrashamTrivedi's repository](https://github.com/PrashamTrivedi/DrawerLayoutTest) The basic code for expandable list view
- [Android Expandable List View Tutorial](http://www.androidhive.info/2013/07/android-expandable-list-view-tutorial/) for editing the ExpandableListView

