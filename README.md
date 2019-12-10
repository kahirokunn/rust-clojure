# Introduction
This is a Clojure Interpreter by Rust.

## Support syntax

```bnf
EXPR := EXPR2

EXPR2 := LPAREN PREFIX_OPERATOR DELIMITER EXPR RPAREN | LPAREN PREFIX_OPERATOR DELIMITER EXPR1 RPAREN

EXPR1 := EXPR1 DELIMITER PRIMITIVE | PRIMITIVE

PRIMITIVE := HISTORY | UNUMBER | \" STR \" | EXPR

UNUMBER := D | UNUMBER D

D := "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"

PREFIX_OPERATOR := RESERVED | OPERATOR

RESERVED := println

OPERATOR := "+" | "-" | "*" | "/"

HISTORY := "*" UNUMBER

DELIMITER := " "

STR := WOLD | UNUMBER | STR WOLD | STR UNUMBER

WOLD := "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m" | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z" | "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M" | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z"

LPAREN := "("

RPAREN := ")"

```
