# calc
used to demonstrate managing go projects (demo 4 / 5) module 3 - see PluralSight

The PluralSight course, Managing Go Projects, changes from the first section on package to the benefits and capabilities of the second section - modules. For any content references or use other than use of this repository, must go to PluralSight and speak with the author of "Managing Go Projects" released in 2023.

In "demo1" to "demo5" in Modules, it used a calc package and showed how it could be deployed as package within same folder as demo module, and later as a package under $GOROOT/src/calc.

Along the way, you got a feel of the ways that a module could call external components and of course that means you could imagine a Sprint by a Scrum team working separately to deliver different value of the overall app that will come together.  Along with the benefits, the author/presenter did a good job of covering the thought processes and any shortcomings that would occur if you had to now have the package or module run on a different machine. 

In "demo6", one solution is to use an external repository -- but instead of staying with the inventory example with simple components -- demo6 reach out to what I thought was an over the top Github respository with so many dependencies. In my opinion, it was just too much -- I don't know the author of the respository "faker" and was not ready to lose focus by doing my normal security due diligence rather than just putting an example together with 'calc' on github.

That's what this is -- just an external placeholder for calc.go from the course to be called, so that all the new lessons on changes to go.mod and the inclusion of go.sum could be understood. 

My session for demo6:
```
cd $GOPATH\src\psmp_2
mkdir psmp206; cd psmp506
touch main.go
go mod init psmp_2.psmp506
vi main.go
go run .
go get github.com/AchieveGoals/calc
cat go.mod
go run .
cat go.sum
```

In main.go, the only change was the ```import (...)``` section
From:
```
import (
  "fmt" 
  
  "calc"
)
```
To:
```
import (
  "fmt"
  
  "github.com\AchieveGoals\calc"
)
```
Note:  the calc.Discount() line didn't change:
```    totalDiscount := calc.Discount(itemPrice, itemDiscount) ```

I mean, how simple has Go made bringing in an external library.

So back to see where demo 7 goes.
