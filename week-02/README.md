[↑ Back](../README.md)

# Week #02

## Topics

Language basics #1 (types, variables, expressions, statements, handling standard I/O, built-in functions, procedures, recursion).

## Agenda

1. The `if` and `if else` statements
1. The `switch` statement

## Sample codes

1. [`calculator_if_01.c`](./samples/calculator_if_01.c)
1. [`calculator_if_02.c`](./samples/calculator_if_02.c)
1. [`calculator_if_03.c`](./samples/calculator_if_03.c)
1. [`calculator_if_04.c`](./samples/calculator_if_04.c)
1. [`calculator_switch_01.c`](./samples/calculator_switch_01.c)
1. [`calculator_switch_02.c`](./samples/calculator_switch_02.c)

## Highlights

### Statement `if else`

1. only one statement or block belongs to the control statement
1. an `else` branch can have a nested `if` statement
1. the previous syntax can be simplified to have an `else if` construct

### About division

The `/` (slash) operator performs an integer division between two integer operands. You must have at least one real (`float` or `double`) operand to get a real result. You can explicitly change a type of an expression by so-called casting its value. Thus, you can use one of the following syntaxes:

1. `(double) a / b`
1. `a / (double) b`
1. `(double) a / (double) b`

Be careful, because syntax `(double) (a / b)` does not work. In this case, you first determine the integer result, then convert it to `double`. Thus, the result would be `2.0` for `5 / 2`.

### Statement `switch`

1. the expression should be implicitly converted to `int`
1. `case` labels have literal values
1. each case can appear only once, the order doesn't matter
1. after evaluating the expression we jump to the corresponding `case`
1. we execute each statement after the `case` label until the first `break` statement or the end of the `switch`'s block

## Required skills

> [!IMPORTANT]
> The next lab will be based on the following expectations. Please ensure that you are aware of all the skills mentioned. Ask your questions using the available Q&A form in Moodle.

1. You must be able to use the `if else` statements.
1. You must be able to use the `switch` statements.
