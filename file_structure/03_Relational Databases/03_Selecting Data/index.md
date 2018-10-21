### Selecting Data
#### Let's see how we can begin to select data from tables through code!

The `select` statement is used to query the database and retrieve data that match what you're looking for and specify!

The format can be shown below:
 ```
 select "column1"
  [,"column2" ,etc]
  from "tablename"
  [where "condition"];
  [] = optional
```
You can select as many column as you would like, or you can use a ``*`` to select all columns.

Conditional selections used in the `where` clause are:   
```
= equal
> greater
< less than
>= Greater than or equal
<= Less than or equal
<> Not equal to
```

The `LIKE` pattern matching operator can also be used in the conditional selection of the where clause. Like is a very powerful operator that allows you to select only rows that are "like" what you specify.

The percent sign "%" can be used as a wild card to match any possible character that might appear before or after the characters specified. For example:

```
select first, last, city
   from empinfo
   where first LIKE 'Ke%';
```
This will match and select any matches of names that start with `Ke`

But remember... `Strings must be in single quotes`!

Or you can specify,
```
select first, last
   from empinfo
   where last LIKE '%o';
```

This statement will match any last names that end in an 'o'.

or..
```
select * from empinfo
   where first = 'Keenan';
```