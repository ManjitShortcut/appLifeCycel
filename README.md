# applifecycle

A new Flutter project.

## Getting Started


App has four state 

1. Resume State (Application in fore groud andaccepeting user input)
2. Inactive State (Application in bacground and receiving event)
3. Pause (Appilcation in background but not receiveubg any event)
4. Suspended (Application is not receiveing background and not in fore groud means app is killed state 

To check we have to widgetbindingObserver

then we have init with widgetbiindingObserver in initState becase initwithState allocated only once
then in depose method we have to delete the observer

initSatate(){
 WidgetsBinding.instance.addObserver(this);
 }
 
 dispose(){
 WidgetsBinding.instance.removeObserver(this);
 }
// Appilcation didchnage lifecycel is method. where we can detect the application lifecycle state.
   @override
  void didChangeAppLifecycleState(AppLifecycleState state) {
    super.didChangeAppLifecycleState(state);
    print(state);
  }



This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
