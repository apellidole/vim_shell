​	

```shell
echo -e "Alice\nBob\nCharlie" > file1.txt
echo -e "Engineer\nDesigner\nManager" > file2.txt

paste file1.txt file2.txt > output.txt
cat output.txt

vim example.txt        # 打开 Vim 编辑器并加载文件
:split                 # 分割窗口为水平窗口
:vsplit                # 分割窗口为垂直窗口
Ctrl + w + w           # 在不同窗口之间切换
:q                     # 关闭当前窗口
:qall                  # 关闭所有窗口并退出 Vim

vim example.txt    # 打开 Vim 编辑器并加载文件
gg=G               # 自动调整整个文件的缩进格式

vim example.txt
:set autoindent
:set smartindent
:set shiftwidth=4
:set tabstop=4
:set expandtab

cat <<EOF > data
Jan2001 100 150 200
Feb2001 110 140 180
Mar2001 120 130 160
Apr2001 130 120 140
May2001 140 110 100
Jun2001 150 100 90
EOF

awk '{print $1,$4,$5}' data | sort --key=2n | head -n 1
awk '{print $1,$4,$5}' data | sort --key=2n | tail -n 1
awk '{print $1,$4,$5}' data | awk '{print $2-$3}' | awk '{s+=$1} END {print s}'



echo -e "apple banana apple orange banana apple orange orange" > input.txt

tr ' ' '\n' < input.txt | sort | uniq -c | sort -nr | head -n 1


echo -e "Name,Age,Occupation\nAlice,30,Engineer\nBob,25,Designer\nCharlie,35,Manager" > input.csv
cut -d ',' -f2 input.csv > output.txt
cat output.txt

```

