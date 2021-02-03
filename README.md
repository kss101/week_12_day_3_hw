# week_12_day_3_hw
Polymorphism &amp; Composition Homework - Quiz

1.	Polymorphism derives from Greek words for “many shapes” or “many forms”.

2.	In Java (and in OO design), polymorphism allows to treat a class as if it were of a different type to its own. This can be done through inheritance using an “abstract” class or, preferably, an interface.

A simple example in JAVA could be to model a LAN, to which we wish to connect different devices, eg printers or laptops. We have a LocalNetwork class, a Printer Class and a Laptop class. We could write an “addTo()” method for our LocalNetwork class so that we can connect a Printer or Laptop to it. But, we’d need one for each device we wished to connect, and keep a list of each type of device:

   e.g. 
   
        devicesLaptop = new ArrayList<Desktop>();
        devicesPrinter = new ArrayList<Printer>();
        public void addTo(Laptop laptop
                devicesLaptop.add(desktop);
            }
        public void addTo(Printer printer){
                devicesPrinter.add(printer);
            }

If we later decide that we want to add different devices, we’d have to write additional addTo() methods and ArrayLists. Instead we can create an “Interface”, say “ICanConnect” and have the LocalNetwork’s method add instances of it.

The code above can become...

    devices = new ArrayList<ICanConnect>();

    public void connect(ICanConnect device){
            devices.add(device); 
        }

 If we then ensure that any device that we wish to connect inherits from “ICanConnect”, then it will be able to connect to the LocalNetwork as any device that is of type ICanConnect can be added... the Laptop is both of type Laptop AND ICanConnect!

3.	As mentioned in the answer to question 2, polymorphism can be implemented through inheritance using an “abstract” class or, preferably, an interface.

4.	When using polymorphism, an object can take on as many “forms” as is needed, but is limited only to those forms from which it inherits.

5.	See answer above for question 2

6.	In OO design, “composition” refers to the idea that an object can be made of other objects. It can be thought of as a “has-a” relationship.

7.	 We might use composition when using inheritance is becoming too unwieldy or limiting due the restricting of inheriting from only one other thing, or, when constructing an object we find that we need access to additional methods from other objects.

8.	An advantage of using composition is that it allows a class to use behaviour from a group of other classes.

9.	When an object is destroyed, the objects of which it is composed are also destroyed.
