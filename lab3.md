# Lab Report 3
In this lab report, the command that I'm going to elaborate on is the ```grep``` command. <br/>
```grep``` searches the keyword in a file and prints out the line containing the keyword. <br/>
For instance: <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:201$ grep "limitation" cc2171.txt 
        This study has a number of limitations. We had
```
There are other modifications to add on to this command for different output. <br/>
The first command-line option is ```-r```. <br/>
Examples: <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:202$ grep -r "limitation" *
1468-6708-3-1.txt:          health status, limitations in activities of daily living
1468-6708-3-1.txt:          Potential limitations
1468-6708-3-10.txt:        as ALLHAT has potential limitations. Built into a structure
1468-6708-3-10.txt:        limitation of physical activity. They are comfortable at
1468-6708-3-3.txt:        a number of inherent study limitations worth noting. First
1468-6708-3-3.txt:        There were also a number of limitations that may have
1471-2091-3-31.txt:          A limitation of our experiments is the restriction of
1471-2105-1-1.txt:        cellular growth upon oxygen limitations (
1471-2105-1-1.txt:        in the table (other than a slight limitation of ATP
1471-2105-1-1.txt:        under oxygen limitation, and this resulted in a decreased
```
The command search every file in the directory biomed and prints out all lines containing the word "limitation". <br/>
We can replace ```*``` with the file-names or file-paths to refer to multiple specific files. <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:204$ grep -r "limitation" gb-2003-4-5-r34.txt gb-2003-4-7-r43.txt
gb-2003-4-5-r34.txt:          false (due to noise in the data, inherent limitations of
gb-2003-4-5-r34.txt:          the data or limitations in the algorithm)? And finally,
gb-2003-4-5-r34.txt:          There are also some limitations with the external
gb-2003-4-7-r43.txt:          limitation, as well as recent findings that carbon source
gb-2003-4-7-r43.txt:        A key limitation of our approach is the use of hexamers,
```
Now it only searches "limitation" in "gb-2003-4-5-r34.txt" and "gb-2003-4-7-r43.txt". <br/>
The ```-r``` option allows us to look through all or few specific files in searching for a keyword. <br/>
