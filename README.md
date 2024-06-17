# Dcit 318 assignment-2
public class Animal {

  public void MakeSound() {
    System.out.println("Some generic sound");
  }
}

public class Dog extends Animal {

  @Override
  public void MakeSound() {
    System.out.println("Bark");
  }
}

public class Cat extends Animal {

  @Override
  public void MakeSound() {
    System.out.println("Meow");
  }
}

public class Main {

  public static void main(String[] args) {
    Animal animal = new Animal(); // Create an Animal object
    Dog dog = new Dog(); // Create a Dog object
    Cat cat = new Cat(); // Create a Cat object

    animal.MakeSound(); // Call MakeSound() on Animal object (prints generic sound)
    dog.MakeSound(); // Call MakeSound() on Dog object (prints Bark)
    cat.MakeSound(); // Call MakeSound() on Cat object (prints Meow)
  }
}








from abc import ABC, abstractmethod

class Shape(ABC):
  @abstractmethod
  def GetArea(self):
    pass

class Circle(Shape):
  def __init__(self, radius):
    self.radius = radius

  def GetArea(self):
    return 3.14159 * self.radius * self.radius

class Rectangle(Shape):
  def __init__(self, width, height):
    self.width = width
    self.height = height

  def GetArea(self):
    return self.width * self.height

# Main method
def main():
  circle = Circle(5)
  rectangle = Rectangle(4, 6)

  print("Area of circle:", circle.GetArea())
  print("Area of rectangle:", rectangle.GetArea())

if __name__ == "__main__":
  main()







public interface Movable {
  public void Move();
}

// Car class implementing Movable
public class Car implements Movable {

  @Override
  public void Move() {
    System.out.println("Car is moving");
  }
}

// Bicycle class implementing Movable
public class Bicycle implements Movable {

  @Override
  public void Move() {
    System.out.println("Bicycle is moving");
  }
}

// Main method to test Movable objects
public class Main {

  public static void main(String[] args) {
    Movable car = new Car(); 
    Movable bicycle = new ;

    car.Move();
    bicycle.Move(); 
  }
}
