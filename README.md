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

  Appilcation didchangelifecycel is method. where we can detect the application lifecycle state. //
  @override
  void didChangeAppLifecycleState(AppLifecycleState state) {
    super.didChangeAppLifecycleState(state);
    print(state);
  }

