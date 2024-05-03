# ELN-Rec
Listing 47 ELN-Rec/Rec.java Page 81

Cont. from [46.ELR-Records](https://github.com/Java-PJATK/46.ELR-Records)  

We defined the `Motorcycle` record in just one line, without adding anything into the body of the class definition. Usually, this is how we define records.  

However,

* it is allowed to add static constants (as `DEF_B` in the example below, line 12), but not non-static fields, not declared in the descriptor of the record;

* we can define “normal” non-static methods (as `getProduct` below, lines 20-22), remembering that they cannot modify non-static fields, which are, by definition, final;

* it is possible to define “manually” constructors with fewer arguments, which, using `this`, must call the canonical constructor (as in lines 17-19);

* we cannot define non-static initializers; however, static initializers are allowed.

Moreover, we can define, at most one, the so called **compact constructor**. An example is shown in lines 13-16. As we can see,

* List of parameters is left out, but they are visible in the body of the compact constructor.

* We can assign values to the fields, but we don’t have to. Here, we assign the value of the doubled argument `a` to the field `a`. We do _not_ assign any value to `b`,
though.
However, if we don’t do it explicitly, compiler will add such assignments just before leaving the body of the compact constructor (so the field `b` _will_ be assigned a value). Usually, compact constructors do not assign any values to the fields explicitly; they are used, e.g., to validate the values of arguments, as in line 15: to the fields

## Listing 47 ELN-Rec/Rec.java

The program prints  

```
R[a=2, b=4]
R[a=4, b=7]
```

Records can be generic (see Sec. ??, p. ??) and can implement interfaces (see Sec. ??, p. ??).

Next [Section 9 Strings and StringBuilders 48.BHH-Strings](https://github.com/Java-PJATK/48.BHH-Strings)
