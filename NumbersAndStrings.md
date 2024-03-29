# Arithmetic operator facts

When a float literal is used in an expression with an integer literal, the result is always a float literal.

remainder only works with integers.

    var (
      num1 = 1
      num2 = 3
      float float64
    )

    float = num1 + num2 -- this doesn't work

    float = float64(num1 + num2) -- it has to be converted

when use float values, the result can be inaccurate!

    ratio := 1.0/10
    fmt.Printf("%.60f", ratio)

the result is not just 0.1, after some decimal places, it looks weird.


# Always use the same type for result and operands to avoid hidden type conversion.

    var ratio float64 = 3/2
    fmt.Println(ratio) //prints 1

  the way go does it is to convert both operands to int and then convert the result to float64.
  the fraction part will be removed after convertion.
  
    ratio = float64(int(3) / int(2))
    fmt.Println(ratio) prints 1
 
# Precedence is as the same as math, if confused always use parentheses.

    celsius := 35.
    
    fahrenheit := (9 * celsius) / 5 + 32
    
    fmt.Printf("%g C is %g F\n", celsius, fahrenheit)







