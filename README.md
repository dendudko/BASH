# Работа с текстом в BASH
## Код
<pre>
<code>
cat file1.txt | tail -n 40 > file2.txt && head -n 10 file2.txt > file3.txt \ 
&& cat file2.txt | grep коко > temp.txt \
&& cat temp.txt | sed 's/коко/куку/g' | head -n 3 >> file3.txt \
&& rm -f temp.txt \
&& sort file3.txt | uniq -c > file3.txt
</code>
</pre>
## Результат работы
<img src="result.png"></img>
## Заметки
Генерировал исходный файл на каком-то сайте, повторяется по 56 строк, в `file3.txt` из-за этого все строки получаются неповторяющимися.
