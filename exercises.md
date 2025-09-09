**Find the FASTA file in the data folder.**
<details> 
  <summary>hint</summary>
  Use `find` command. To se help, use `find --hep`. For a full manual, check `man find`.   
</details>
<details> 
  <summary>answer</summary>
   `find data -iname "*.fasta"`
</details>
<details> 
  <summary>explain answer</summary>
   `find` is the command for finding files or directories.
   `data` is the name of the directory to search.
   `-iname` or `-name` is the name to search. `-name` is case sensitive and `-iname` is case insensitive.
   `"*.fasta"` is the search pattern. `*` is a wildcard. In `bash` and `find` it means one or more of any character, but in `regex` it means only one of any character. The quotes are important here. If we write `*.fasta` without the quotes, then the shell will interpret the expression. If we write `"*.fasta"` with the quotes then `find` will interpret the expression, which is what we want here.
</details>
<details> 
  <summary>explain quotes in more detail</summary>
   If we use `*.fasta` without quotes, then the shell will do [wildcard expansion](https://tldp.org/LDP/abs/html/globbingref.html). That means, if there are any files which end with `.fasta` in the current directory, the shell wil replace `*.fasta` with thir filenames. So your command `find data -iname *.fasta` might turn into `find data -iname Platynereis.fasta Drosophila.fasta` if files Platynereis.fasta and Drosophila.fasta are in your current directory. If there are no .fasta files in your current directory, then the shell has nothing to expand and will pass the expression `*.fasta` to `find` as is, and the `find` command will work as expected. The quotes tell the shell not to do wildcard expansion even if there are .fasta files in the current directory. 
</details>
<br>

**Which tool would you use to check the contents and why?**
<details> 
  <summary>answer</summary>
   `head` or `less`. Fasta files are very large and take a long time to open with a standard text editor.
   `head` shows only the first few lines of a file.
   `less` reads the file into memory only one page at a time.
</details>
<br>

**How do you exit `less`?**
<details> 
  <summary>answer</summary>
   Q key 
</details>
<br>

**Find the file about Platynereis.**
<details> 
  <summary>answer</summary>
   `grep -r Platynereis`
</details>
<br>

**Find image 8_9_1.jpg.**
<details> 
  <summary>hint</summary>
   Use the same strategy as in the first question.
</details>
<br>

**Identify what kind of image is 8_9_1.jpg.**
<details> 
  <summary>hint</summary>
   Use `identify` from imagemagick suite.
</details>
<br>


**Divide image 8_9_1.jpg into 4 tiles.**
<details> 
  <summary>hint</summary>
  Use `convert` from imagmagick suite. Read the manual with `man convert`.
</details>
<details> 
  <summary>hint</summary>
  The full command you need is in a file in this repository.   
</details>
<br>

**Stitch the tiles back together.**
<details> 
  <summary>hint</summary>
  Use `montage` from imagmagick suite.   
</details>
<details> 
  <summary>hint</summary>
  The full command you need is in a file in this repository.   
</details>
<br>

**What kind of file is 7_2_1.jpg?**
<details> 
  <summary>hint</summary>
  What does `identify` say?
</details>
<details> 
  <summary>hint</summary>
  Try `file` command.   
</details>
<br>
