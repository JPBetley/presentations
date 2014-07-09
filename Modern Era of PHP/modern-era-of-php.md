#The Modern Era of PHP

---

##Phil Betley
###@jpbetley
###github.com/jpbetley
###phil@phproc.com

---

#My Story

---

#How Did We Get Here? 

---

![](images/rasmus.jpg)
^http://buytaert.net/sites/buytaert.net/files/cache/drupalcon-sunnyvale-2007-rasmus-lerdorf-700x700.jpg

^Rasmus Lerdorf started PHP in 1994 as a set of CGI binaries written in C. The syntax we know today wasn't introduced until 1998.

---

![](images/zend.jpg)
^http://mayeul.com/uploads/2010/09/zend-php-company.jpg

^PHP 4 introduced the Zend Engine, which is the engine that is still used today by most PHP applications. It introduced a lot of new features, but it was still a largely procedural language.

---

#PHP 5

^PHP 5 introduced a lot of great features that built into what I call modern PHP.

---

###PHP 5 Features
- Standard PHP Library
- Type hinting
- Exception Classes
- PDO

---

###PHP 5 Object Model
- Classes (abstract) and interfaces
- Static Methods
- Magic Methods
- Autoload Method
- Zend Engine 2

^ This was the beginning of object oriented programming in PHP. With the introduction of a fully functional object model, we could build much richer and encapsulated applications. This also gave rise to the usage of Design Patterns within PHP.

---

###PHP 5.1
- Date library overhaul
- Performance improvements (carries with each version)
- PDO enabled by default

---

###PHP 5.2
- Better memory management
- JSON support
- Zip extension
- Input filtering
- File upload progress tracking

---

###PHP 5.3
- Namespaces
- Late static binding
- Lambda and closure support
- Optional garbage collection
- Syntax additions

^Syntax - ternary operator, __callStatic(), etc

^This is the true start of Modern PHP. With the introduction of the myriad of features introduced in this version, devs were allowed to do much more than before.

---

###PHP 5.4
- Traits
- New array syntax
- Built-in web server
- Closures support `$this`

--- 

###PHP 5.5
- Zend OPCache
- Password hashing API
- Generators
- `finally` keyword

---

#Object Oriented Programming

^With the new features that have been continuously added throughout the lifetime of PHP 5, PHP devs have been making a transition to using more OOP practices and design patterns

---

###Design Patterns
- Factory
- Iterator
- Decorator
- Front Controller
- Model-View-Controller

---

# Autoloading

^Also included with new versions of PHP is the capability to do class autoloading. Before this, we'd have to require/include every php file we needed in order to use it.

---

# `__autoload()` Changed Everything

---

# Page Controller Pattern

^The page controller pattern is probably the way most of us did things back when we started toying around with php. When we needed a new page, we created a new .php file, and someone would navigate to that page in a browser.

---

# Front Controller Pattern

^We replaced that with the front controller pattern. This pattern basically gave us the ability to send all requests to a single file - the front controller. And it would handle the requests off to the places we wanted it to go. Now we could keep all of our code hidden from the web server, and only keep the front controller in our public web root.

---

# The Rise of the Frameworks

---

###Security Concerns
- Cross-site scripting
- Cross-site request forgery
- SQL injection
- Session hacking

^These can be prevented with two main security measures, filtering input, and escaping output.

---

###Version Control
- Git
- Mercurial
- Subversion

---

#Github and Bitbucket

---

