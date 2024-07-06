using System;

// Abstract class Shape
abstract class Shape
{
    // Abstract method to get area, to be implemented by derived classes
    public abstract double GetArea();
}

// Derived class Circle inheriting from Shape
class Circle : Shape
{
    // Radius of the circle
    public double Radius { get; set; }

    // Constructor to initialize radius
    public Circle(double radius)
    {
        Radius = radius;
    }

    // Implementation of GetArea method for Circle
    public override double GetArea()
    {
        return Math.PI * Radius * Radius;
    }
}

// Derived class Rectangle inheriting from Shape
class Rectangle : Shape
{
    // Width and height of the rectangle
    public double Width { get; set; }
    public double Height { get; set; }

    // Constructor to initialize width and height
    public Rectangle(double width, double height)
    {
        Width = width;
        Height = height;
    }

    // Implementation of GetArea method for Rectangle
    public override double GetArea()
    {
        return Width * Height;
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create an instance of Circle
        Circle circle = new Circle(5);
        Console.WriteLine($"Circle Area: {circle.GetArea()}");

        // Create an instance of Rectangle
        Rectangle rectangle = new Rectangle(4, 6);
        Console.WriteLine($"Rectangle Area: {rectangle.GetArea()}");
    }
}
