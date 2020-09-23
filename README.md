<div align="center">

## How to Bubble\-Sort a Vector


</div>

### Description

I was curious if you could even do this in Java (sort a vector). I guess I proved to myself that you can. Please vote.
 
### More Info
 
Just input any numbers in the dialog box that pops up, then -99 to get the results.

Just compile and run!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Eric Larson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/eric-larson.md)
**Level**          |Intermediate
**User Rating**    |4.3 (13 globes from 3 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/eric-larson-how-to-bubble-sort-a-vector__2-2058/archive/master.zip)





### Source Code

```
//How to Bubble-sort a vector in java
import java.lang.*;
import javax.swing.*;
import java.util.*;
public class chapter4
{
 public static void main(String argv[])
 {
  String sInput;
  final Vector v = new Vector(1);
  int x, one1, two2;
  Integer iInput;
  Integer bInput1;
  Integer cInput2;
  boolean unsorted = true;
  int last, last2;
  sInput = JOptionPane.showInputDialog("enter number or -99");
  iInput = new Integer(sInput);
  x = Integer.parseInt(sInput);
  while ( x != -99)
  {
   v.addElement(iInput);
   sInput = JOptionPane.showInputDialog("enter number or -99");
   iInput = new Integer(sInput);
   x = Integer.parseInt(sInput);
  }
  //sorting starts here
  for(int pass = 0; pass < v.size() -1 && unsorted; pass++)
  {
   unsorted = false;
   last = v.size()- 1;
   //last--;
   for( int i =0; i < last; i++)
   {
   //bInput1 = v.elementAt(i);// ERROR MESSAGE:
   //Explicit cast needed to convert java.lang.Object to java.lang.Integer
   //must be type cast from Object to Integer like the lines below.
   bInput1 = (Integer)v.elementAt(i);
   cInput2 = (Integer)v.elementAt(i + 1);
   one1 = bInput1.intValue();
   two2 = cInput2.intValue();
   if(one1 < two2)
   {
    v.setElementAt(v.elementAt(i + 1), i);
    v.setElementAt(bInput1, i + 1);
    unsorted = true;
   }
   }
   last--;
  }
  JOptionPane.showMessageDialog(null, "largest: " + v.elementAt(0) + "\n" +
   "Second: " + v.elementAt(1) + "\n" + "Number: " + v.size()+ "\n" +
   "" + v.toString());
  System.exit(0);
 }
}
```

