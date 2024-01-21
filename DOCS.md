# Documentation
### Keywords (real important)
```print <text: TStr>``` (```println <text: TStr>```) - write to the standard output<br>
```scanln <varname: Identifier>``` - read from standard input<br>
```var <varname: Identifier> <operator: Op> <value: TStr | TInt | TFloat(?)>``` - assign a value to variable<br>
```return <value: Identifier | TStr | TInt | TFloat(?)>``` - return value from function<br>
```cast <varname: Identifier> <type: str | int | float(?)>``` - convert a variable to another type<br>
```free <varname: Identifier>``` - delete variable<br>
```fn <name: Identifier>``` - define a function<br>
```len <varname: Identifier> <strname: Identifier>``` - get length of strname and store it in varname<br>
```getchar <strname: Identifier> <index: TInt> <varname: Identifier>``` - get a character from strname[index] and store it in varname<br>
```__pyexec <code: TStr>``` - execute python code<br>
```setchar <strname: Identifier> <char: TStr> <index: TInt>``` - set strname[index] to char<br>
```nf``` - end function definition<br>
```call <name: Identifier>``` - call function<br>
```namespace <name: Identifier>``` - define a namespace<br>
```nsEnd``` - end namespace definition<br>
```exit <code: TInt>``` - exit with errorlevel<br>
```sleep <seconds: TInt | TFloat(?)>``` - sleep for N seconds<br>
```utime <varname: Identifier>``` - get current unix time and store it in varname<br>
```cp <varname: Identifier> <copyname: Identifier>``` - get a value from copyname and store it in varname<br>
```?``` - define a comment<br>
```-?``` - end comment definition<br>
```if``` - if statement no need to explain<br>
```else``` - else statement for if statement<br>
```end``` - end if statement<br>
that's it yay

Down there will be code examples, Indents are not important, but are recommended to use. Code line that explained before would not be explained
### Hello world
```
fn main;                   ? define a main function -?
  println "Hello, world!"; ? print hello world -?
  return 0;                ? exit with code 0 -?
nf;                        ? close main function -?
```

### Variables
```
fn main;
  var a = 123;        ? define a variable named 'a' and assign a value 123 to it -?
  var a + 1;          ? increment 'a' by 1 -?
  println "Result: $a^";  ? output the result -?
  return 0;
nf;
```

### Input
```
fn main;
  print "Type something: ";
  scanln input;            ? Get a string from user and store it in 'input' -?
  println "You typed: $input^";
  return 0;
nf;
```

### Type converting
```
fn main;
  var a = "123";
  cast a int;
  var a + 1;
  println "Result: $a^";
  return 0;
nf;
```

### Functions
Before continuing, I will just let you know that there is a reserved variables for functions like: ret, arg1, arg2, arg3, arg4, arg5. And these variables cannot be deleted
```
fn add;
  var arg1 + arg2;
nf;

fn main;
  var arg1 = 123;
  var arg2 = 1;
  call add;

  println "Result: $arg1^";
nf;
```

### Namespaces
```
namespace myNamespace; ? define a namespace called myNamespace -?

  fn sayhello;
    println "Hello, world!";
  nf;

nsEnd;                 ? stop namespace definition -?

fn main;
  call myNamespace::sayhello;
nf;
```
