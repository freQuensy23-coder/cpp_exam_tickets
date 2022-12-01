# Good (OOP, stl libraty)
## Encapsulation
Encapsulation -  refers to the bundling of data with the methods that operate on that data, or the restricting of direct access to some of an object's components. Other meaning ob this world is hidding data in private blocks in classes and creating special methods (setters and getters) to acces it. It helps us to hide some fields from unauthorized access or check data before put it to class fields. Examples
```C++ 
class Point{
int x;
int y;
public:
void set_point_x(int x){
	if (x < 0) or (x > 1980){
		throw std::invalid_argument("poin is not in the screen");
	}}
```

```C++
class DateParser{
	webRequester req;
	htmlParser parser;
public:
	int get_date(){
		answer = req.get_api();
		time = parser.parse();
		return time;
	}}

There are three types of access modifiers:

* public - this fields and methods could be accessed outside the class
* private - this fields and methods could **not** be accessed outside the class, but could be used in all methods
* protected -  access to class members in the member-list up to the next access specifier (public or private) or the end of the class definition. (Private, but can be public for "children" of this class)

## Inheritance 
Inheritance is the mechanism of basing an object or class upon another object or class, retaining similar implementation. It helps us to create similar realisation of some objects.
```C++
class Velchie // Abstract car
{
	int number;
	public:
	virtual void drive() = delete;
} 

class Car : public Velchie
{ 
	public:
	void drive(){cout << "Vhvhvhvhhv" << endl;
}
```
In this case number integer field will be private field of Car class. Also virtual method "drive" has been overrided in Car class. 

There are 3 types of inheritance, differ in how access modifiers will change (table).
![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/table-class.png)

## Polymorphism
Idea of polymorphism is that the same entity (function or object) behaves differently in different scenarios. For example if player class has shoot method with gun parameter, we can pass an mashine gun object to this function, if mashine gun class have been inheritanced from gun one.

Also functions overriding sometimes referred to polymorphysm too.


## Constructors and destructors
Sometimes class instances need some additional information to initialise (for ex. point need it's coordinates, name; planet need orbit information, etc).
By default all classes have zero patameters initialiser, but we can implement custom one use this syntax:
```C++
class Point{
	..\\..
	public:
	Point(int x, int y){
		x = x;
		y = y;
		renderer->fill_pixel(255,255,255, x,y)
	} 	

}
```

