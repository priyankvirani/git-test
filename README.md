Email : priyankvirani52@gmail.com


Descriptive Questions:

1- Can we nest the Scaffold widget? Why or Why not?

scaffold was single common material base widget and it's typically not necessary to nest scaffolds.
gives you many basic functionalities, like AppBar, BottomNavigationBar, Drawer, FloatingActionButton, etc.

2- How to reduce the rebuilding of the widget?

flutter provide you setState() to refrence the state info object and idenify any changes to the current state this one can handle these changes and rebuild app

3-How can I access platform(iOS or Android) specific code from Flutter?

using flutter method channel 

IOS - Flutter <- Flutter Method Channel <--> AppDelegate <--> IOS platfrom api or 3rd party apis for ios

Android- Flutter <- Flutter Method Channel <--> Activity <--> Android platfrom api or 3rd party apis for Android 

4- What is BuildContext? What is its importance?

BuildContext?  was use for locat the used to trck all user which part of widget tree and we can che the position on widget tree 
when that widget was appear on screen. each and every widgets is passed to their build method. this was importance becouse each build context 
is unique toa widget


Coding Questions:

1 - In the below code, list1 declared with var, list2 with final and list3 with const. What is
the difference between these lists? Will the last two lines compile?

- for var keyword the data type can be change.except that you declare on this manager data type

List<String> list1 = ['I', '💙', 'Flutter'];

with final and const you can't reasssing and new value the initial assigmen.
final value are asssigned once at runtimr and const value has to be either decalre at compile timeor static or hard codedd beforee app is in runnning sttae

for the list while compile the code you can not reassigning the list2 list itself but you can change pisuition of third index.

if tried to compile this line list2 = ['I', '💙', 'Dart']; you can not becouse you're trynig to reassign final variable
also const list3 = list1; this line also not compile because  the value list 1 not assignes until runtime.

2- Identify the problem in the following code block and correct it.
- return with MEMORY_EXCEEDED error 


3-What is the main difference between Mobx & Provider? Can we use both together?
Write code to demonstrate it.

provide use only for depedency injection with mobx it isno use for state changes 

for the mobx use we don't need and statefull widget in most cases becouse you are hanbding state changes 
inside mobx controller and any changes in state we use observer to change ui

class MyStore = _MyStore with _$MyStore;

abstract class _MyStore with Store {

_MyStore(){
  getData();
}
}

