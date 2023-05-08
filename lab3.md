# Lab Report 3
In this lab report, the command that I'm going to elaborate on is the ```grep``` command. <br/>
```grep``` searches the keyword in a file and prints out the line containing the keyword. <br/>
For instance: <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:201$ grep "limitation" cc2171.txt 
        This study has a number of limitations. We had
```
There are other modifications to add on to this command for different output. <br/>
<br/>
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
For the sake of simplicity only the first 10 lines are shown here. <br/>
The command search every file in the directory biomed (or subdirectory if any) and prints out all lines containing the word "limitation". <br/>
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
<br/>
The second command-line option is ```-c```. <br/>
Examples: <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:205$ grep -c "limitation" *
1468-6708-3-1.txt:2
1468-6708-3-10.txt:2
1468-6708-3-3.txt:2
1468-6708-3-4.txt:0
1468-6708-3-7.txt:0
1471-2091-2-10.txt:0
1471-2091-2-11.txt:0
1471-2091-2-12.txt:0
1471-2091-2-13.txt:0
1471-2091-2-16.txt:0
```
The command search every file in hte directory and prints out of the number of times keyword "limitation" appears in each file. <br/>
We can replace ```*``` with the file-names or file-paths to refer to multiple specific files. <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:206$ grep -c "limitation" gb-2003-4-5-r34.txt gb-2003-4-7-r43.txt
gb-2003-4-5-r34.txt:3
gb-2003-4-7-r43.txt:2
```
Now it only searches "limitation" in "gb-2003-4-5-r34.txt" and "gb-2003-4-7-r43.txt". <br/>
The ```-c``` option allows us to look through all or few specific files and indicate which files have considerable amount of keywords. <br/>
<br/>
The third command-line option is ```-v```. <br/>
Examples: <br/>
```
[cs15lsp23oz@ieng6-202]:biomed:209$ grep -v "i" gb-2003-4-5-r34.txt




        Background

          or Sharan
          data).
          sample 'A'. However, before one does subsequent


          Related work
          Hughes
          et al . [ 18 ] have taken a


          to known external knowledge of the data); and cluster
          accurate and more stable clusters. When repeated
          repeated measurements. The model-based approaches
          more stable clusters.



        Results

          remeasures the array data, how often are objects


          subtrees) to form a dendrogram. To evaluate cluster
          study.


          measurements

            Average over repeated measurements


            et al . [ 2 ] proposed an
            et al . [ 2 ] developed an error
            the repeated measurements for these two genes.
 ```
 Another:
 ```
 [cs15lsp23oz@ieng6-202]:biomed:222$ grep -v "i" rr166.txt




        (TX)A
        2 ) decreases smooth muscle cell



          by Kumar
          they became confluent. On passage 4 the cells were
          cells were thawed, cultured and passed at least once. All
          to 8.
 ```
 The command line search the file prints out all line without "i". <br/>
 This helps us quickly identify the lines without the keyword. We could also replace the file-name with ```*``` to search all files in directory.
 
 The last command-line option is ```-w```.
 Examples:
 ```
 [cs15lsp23oz@ieng6-202]:biomed:223$ grep -w "limitation" *
1468-6708-3-10.txt:        limitation of physical activity. They are comfortable at
1471-2091-3-31.txt:          A limitation of our experiments is the restriction of
1471-2105-1-1.txt:        in the table (other than a slight limitation of ATP
1471-2105-1-1.txt:        under oxygen limitation, and this resulted in a decreased
1471-2105-3-12.txt:        being pursued with urgency. One known current limitation in
1471-2105-3-16.txt:        A potential limitation of the original kernel document
1471-2105-3-16.txt:        Finally, it is important to take note of the limitation
1471-2105-3-2.txt:            platforms. (Note: due to a limitation in the web server
1471-2105-3-2.txt:            limitation can be avoided by subdividing large
1471-2105-3-2.txt:            limitation, we have utilized comparative analysis to
1471-2105-3-28.txt:          for overcoming this limitation will now be presented.
1471-2105-3-28.txt:          Under the finite word length limitation we note that
1471-2105-3-28.txt:          length overcomes the finite word length limitation and
```
The command line shows lines matching the exact keyword. Comparing to the search in first example, lines containing solely "limitations" aren't shown here.
```
[cs15lsp23oz@ieng6-202]:biomed:224$ grep -w "limitation" gb-2003-4-5-r34.txt gb-2003-4-7-r43.txt
gb-2003-4-7-r43.txt:          limitation, as well as recent findings that carbon source
gb-2003-4-7-r43.txt:        A key limitation of our approach is the use of hexamers,
```
Same thing for searching in specific files.
```-w``` helps us to eliminate inaccurate searches which contain the keyword as part of another words.
This is the end of the lab report.

Sources: <https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix>
