<div align="center">

## Boolean function that compares two files to see if they are identical


</div>

### Description

This boolean function simply reads in two files and compares them to see if they are the same. It returns true if they are and false if they aren't. I quickly wrote this up to compare text files against template files.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[BP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/bp.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/bp-boolean-function-that-compares-two-files-to-see-if-they-are-identical__1-24305/archive/master.zip)





### Source Code

```
Public Function compare_files(fileOne As String, fileTwo As String) As Boolean
  Dim fileOneContent As String
  Dim fileTwoContent As String
  Dim temp As String
  Open fileOne For Input As #1
  Do Until EOF(1)
    Line Input #1, temp
    fileOneContent = fileOneContent + temp
  Loop
  Close #1
  Open fileTwo For Input As #1
  Do Until EOF(1)
    Line Input #1, temp
    fileTwoContent = fileTwoContent + temp
  Loop
  Close #1
  If fileOneContent = fileTwoContent Then
    compare_files = True
  Else
    compare_files = False
  End If
End Function
```

