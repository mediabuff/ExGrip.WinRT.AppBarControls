ExGrip.WinRT.AppBarControls
===========================

SpliButton for Windows 8.1 to be used with AppBars (Top) appbar similar to the Microsoft Weather app

![splitbuttonsample](https://cloud.githubusercontent.com/assets/1821384/4431832/f888855c-467a-11e4-942d-d096baa3cfec.png)


Properties that directly influence the visual apperance of the control
======================================================================



![mainproperties](https://cloud.githubusercontent.com/assets/1821384/4431914/1dd0f59e-467e-11e4-93d0-373633bd19ee.png)


Properties that influence the behaviour of the control
======================================================================

*ToggleOnParentFocusChange (bool)*

When selected (true), updates the  "RightToggle" property after the parent (for example the AppBar) looses focus. You can bind the Visibility property (using a converter boolean2visibiliy) of any FrameworkElement to hide/show it after the parent element looses focus. In the sample the third SplitButton is using this property (set to true) to show a StackPanel when the toggle-button is pressed. When the app-bar looses focus, the StackPanel disappears as well, and the toggle-button is reset to its initial state (arrow-down).

The second button has set the ToggleOnParentChange propery de-selected (false). Therefore the Button that appears when you hit it's toggle-button will stay there (even when the app-bar is not visible) and the toggle-button will be shown in it's last position (arrow-up, or arrow-down). This allows you to keep the elements to be shown in a visible state.


![toggleonfocuschange](https://cloud.githubusercontent.com/assets/1821384/4432000/524efcfa-4681-11e4-8a97-1bd467862004.png)


Events and Binding using MVVM
=============================

You can work with the control using  standard events (for code-behind) or commands for MVVM.

*Commands*

* LeftAreaMouseDownCommand and LeftAreaMouseDownCOmmandParameter (when the user clicks on the left button)
* ToggleButtonClickedCommand and ToggleButtonClickedCommandParameter (when the user clicks the toggle-button)

*Events*

* LeftAreaButtonClicked (when the user clicks on the left button)
* ToggleAreaButtonClicked (when the user clicks the toggle button)


Visual States
=============
The SplitButton has the following VisualStates that can be used for customizations:

*Visiual-State-Group "RightAreaStates"*

* RightAreaNormal - state for the toggle-button in "normal" state
* RightAreaHover - the "mouser-over" state
* RightAreaHoverOut - the "mouse-out" state
* RightAreaMouseDown - the "clicked" state
* RightAreaMouseUp - the state when your finger leaves the left mouse button
* ReightToggle - the "toggle-button toggle" state
* RightHoverToggle - the "mouse-over" when in toggle mode

*Visual-State-Group "LeftAreaStates"*

* LeftAreaNormal - the button is in an "untouched" state
* LeftAreaHover  - the "mouse-over" state
* LeftAreaHoverOut - the "mouse-out" state
* LeftAreaMouseDown - the "clicked" state
* LeftAreaMouseUp - the state when your finger leaves the left mouse button

You can open the sample project in Expression Blend for VS 2013 and edit the "Default" style that you can find in Main.xaml (within the Page-Resources).


Helper
=================

> [Helper for online usage](http://htmlpreview.github.io/?https://github.com/Injac/ExGrip.WinRT.AppBarControls/blob/master/Helper/WebSite/Index.html)


> [Helper for offline usage](https://github.com/Injac/ExGrip.WinRT.AppBarControls/raw/master/Helper/AppBarCustomization.chm)


How to contribute
=================

There is a *dev-branch* that was setup especially for contributions, to merge any additions in the future with the master-branch. Please use this branch to issue your pull-requests.

TO-DO'S
======
* Setup Wiki
* Enhance Documentation 
* Code Reviews
* Setup Nuget-Packaging 
* Re-work solution structure

LICENSE
=======

*The MIT License (MIT)*

Copyright (c) <year> <copyright holders>

Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
 all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.


