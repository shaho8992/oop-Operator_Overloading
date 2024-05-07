# oop-Operator_Overloading

//using System;
//using System.Collections.Generic;
//using System.Linq;
//using System.Text;
//using System.Threading.Tasks;

//namespace Operator_Overloading
//{


//    // A three-dimensional coordinate class.
//    class ThreeD
//    {
//        int x, y, z; // 3-D coordinates
//        public ThreeD() { x = y = z = 0; }
//        public ThreeD(int i, int j, int k) { x = i; y = j; z = k; }
//        // Overload binary +.
//        public static ThreeD operator +(ThreeD op1, ThreeD op2)
//        {
//            ThreeD result = new ThreeD();
//            /* This adds together the coordinates of the two points
//            and returns the result. */
//            result.x = op1.x + op2.x; // These are integer additions
//            result.y = op1.y + op2.y; // and the + retains its original
//            result.z = op1.z + op2.z; // meaning relative to them.
//            return result;
//        }
//        // Overload binary -.
//        public static ThreeD operator -(ThreeD op1, ThreeD op2)
//        {
//            ThreeD result = new ThreeD();
//            /* Notice the order of the operands. op1 is the left
//            operand and op2 is the right. */
//            result.x = op1.x - op2.x; // these are integer subtractions
//            result.y = op1.y - op2.y;
//            result.z = op1.z - op2.z;
//            return result;
//        }
//        // Show X, Y, Z coordinates.
//        public void Show()
//        {
//            Console.WriteLine(x + ", " + y + ", " + z);
//        }
//    }



//    internal class Program
//    {
//        static void Main(string[] args)
//        {


//            ThreeD a = new ThreeD(1, 2, 3);
//            ThreeD b = new ThreeD(10, 10, 10);
//            ThreeD c;
//            Console.Write("Here is a: ");
//            a.Show();
//            Console.WriteLine();
//            Console.Write("Here is b: ");
//            b.Show();
//            Console.WriteLine();
//            c = a + b; // add a and b together
//            Console.Write("Result of a + b: ");
//            c.Show();
//            Console.WriteLine();
//            c = a + b + c; // add a, b, and c together
//            Console.Write("Result of a + b + c: ");
//            c.Show();
//            Console.WriteLine();
//            c = c - a; // subtract a
//            Console.Write("Result of c - a: ");
//            c.Show();
//            Console.WriteLine();
//            c = c - b; // subtract b
//            Console.Write("Result of c - b: ");
//            c.Show();
//            Console.WriteLine();

//        }
//    }

//}
/////////////////////////////////////////////////////////////////////////////////////////

//////////////////////////////////////Overloading Unary Operators
//////    public static ThreeD operator -(ThreeD op)
//////{
//////    ThreeD result = new ThreeD();
//////    result.x = -op.x;
//////    result.y = -op.y;
//////    result.z = -op.z;
//////    return result;
//////}

/* Handling Operations on C# Built-in Types (I)
    / Overload binary + for ThreeD + int.
public static ThreeD operator +(ThreeD op1, int op2)
{
    ThreeD result = new ThreeD();
    result.x = op1.x + op2;
    result.y = op1.y + op2;
    result.z = op1.z + op2;
    return result;
}
*/

////////////////////////////////////////////////////////////////////////////////////

/*using System;
{ 
    namespace kurd

// Overload binary + for ThreeD + int.
public static ThreeD operator +(ThreeD op1, int op2)
{
    ThreeD result = new ThreeD();
    result.x = op1.x + op2;
    result.y = op1.y + op2;
    result.z = op1.z + op2;
    return result;
}
static void Main(string[] args)
{

    ThreeD b = new ThreeD(10, 10, 10);
    ThreeD c;
    //  c = b + 5; // add a and b together
    c = b + 5;
    Console.Write("Result of b + 5: ");  // 15, 15, 15 
    c.Show();
}
}
*/

/////Overloading the Relational Operators (II)
///

// A three-dimensional coordinate class.


//////////////////////////////////////////////////////////////////////////////

/*
using System;

///
class ThreeD
{
    int x, y, z; // 3-D coordinates
    public ThreeD() { x = y = z = 0; }
    public ThreeD(int i, int j, int k) { x = i; y = j; z = k; }
    // Overload <.
    public static bool operator <(ThreeD op1, ThreeD op2)
    {
        if (Math.Sqrt(op1.x * op1.x + op1.y * op1.y + op1.z * op1.z) <
        Math.Sqrt(op2.x * op2.x + op2.y * op2.y + op2.z * op2.z))
            return true;
        else
            return false;
    }
    // Overload >.
    public static bool operator >(ThreeD op1, ThreeD op2)
    {
        if (Math.Sqrt(op1.x * op1.x + op1.y * op1.y + op1.z * op1.z) >
        Math.Sqrt(op2.x * op2.x + op2.y * op2.y + op2.z * op2.z))
            return true;
        else
            return false;
    }
    // Show X, Y, Z coordinates.
    public void Show()
    {
        Console.WriteLine(x + ", " + y + ", " + z);
    }
}

internal class Program
{
    static void Main(string[] args)
    {
        ThreeD a = new ThreeD(5, 6, 7);
        ThreeD b = new ThreeD(10, 10, 10);
        ThreeD c = new ThreeD(1, 2, 3);
        ThreeD d = new ThreeD(6, 7, 5);
        Console.Write("Here is a: ");
        a.Show();
        Console.Write("Here is b: ");
        b.Show();
        Console.Write("Here is c: ");
        c.Show();
        Console.Write("Here is d: ");
        d.Show();
        Console.WriteLine();
        if (a > c) Console.WriteLine("a > c is true");
        if (a < c) Console.WriteLine("a < c is true");
        if (a > b) Console.WriteLine("a > b is true");
        if (a < b) Console.WriteLine("a < b is true");
        if (a > d) Console.WriteLine("a > d is true");
        else if (a < d) Console.WriteLine("a < d is true");
        else Console.WriteLine("a and d are same distance from origin");
    }
}
*/


/////////////////////////////////////////////////////////////////////////////////////////////

/*
using System;

///
class ThreeD
{
    int x, y, z; // 3-D coordinates
    public ThreeD() { x = y = z = 0; }
    public ThreeD(int i, int j, int k) { x = i; y = j; z = k; }

    // Overload true.
    public static bool operator true(ThreeD op)
    {
        if ((op.x != 0) || (op.y != 0) || (op.z != 0))
            return true; // at least one coordinate is non-zero
        else
            return false;
    }
    // Overload false.
    public static bool operator false(ThreeD op)
    {
        if ((op.x == 0) && (op.y == 0) && (op.z == 0))
            return true; // all coordinates are zero
        else
            return false;
    }

    // Overload unary --.
    public static ThreeD operator --(ThreeD op)
    {
        ThreeD result = new ThreeD();
        // Return the decremented result.
        result.x = op.x - 1;
        result.y = op.y - 1;
        result.z = op.z - 1;
        return result;
    }

    public void Show()
    {
        Console.WriteLine(x + ", " + y + ", " + z);
    }
}

internal class program
{
    static void Main(string[] args)
    {
        ThreeD a = new ThreeD(5, 6, 7);
        ThreeD b = new ThreeD(10, 10, 10);
        ThreeD c = new ThreeD(0, 0, 0);
        Console.Write("Here is a: ");
        a.Show();
        Console.Write("Here is b: ");
        b.Show();
        Console.Write("Here is c: ");
        c.Show();
        Console.WriteLine();
        if (a) Console.WriteLine("a is true.");
        else Console.WriteLine("a is false.");
        if (b) Console.WriteLine("b is true.");
        else Console.WriteLine("b is false.");
        if (c) Console.WriteLine("c is true.");
        else Console.WriteLine("c is false.");
        Console.WriteLine();
        Console.WriteLine("Control a loop using a ThreeD object.");
        do
        {
            b.Show();
            b--;
        } while (b);

    }
}
*/

