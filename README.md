<div align="center">

## Int  To String


</div>

### Description

Upss.. I'm really sorry I changed the Title, it was String to Int, but my function is to convert an Int Value to a String Value *sorry* :)

Well, there are two functions I'll post, I think they are very helpfull and I haven't found much informations about it.

//The first an main Function is a Function to Convert an Integer to String. But for this I also needed a function to get the length of an Integer, so I also wrote an extra function for this.
 
### More Info
 
//Input for IntToString = Integer Value

//Input for IntLen = Integer Value

//Return for IntToString = String Value

//Return for IntLen = Integer Value


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Morti](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/morti.md)
**Level**          |Advanced
**User Rating**    |3.7 (26 globes from 7 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Algorithms](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithms__3-29.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/morti-int-to-string__3-8216/archive/master.zip)

### API Declarations

```
#include <string>
#include <stdlib.h>
using namespace std;
```


### Source Code

```
//Function to return the Length of an Integer
int IntLen(int value){
 int div=1;
 int len=1;
 do{
 div*=10;
 if ((int) ( (double)value / (double)(div)) ==0){
 return len;
 }
 len +=1;
 }while(true);
}
//Function to Convert an Integer to String
string IntToString(int value){
 string number;
 int temp;
 bool neg= false;
 //Proof if the number has a negiote sign
 if ((value * (-1)) > value){
 value *=-1;
 neg=true;
 }
 for (int z = IntLen(value) ;z>=1;z--){
 //Modulo to get the last number
 temp = value % 10;
 //add Number to the String
 number = ((char)(temp + 48))+ number;
 //Substract the last number from the Ingeter
 value = (value - temp) /10;
 temp *= 10 ;
 }
 //Set the sign again
 if (neg==true){ number="-" + number; }
 return number;
}
```

