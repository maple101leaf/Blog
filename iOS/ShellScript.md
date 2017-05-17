# Smith-ShellScript

## 如下部分是自己收集的ShellScript脚本块

#### 版本自动递增脚本，例如：1.0 => 1.1， 1.9 => 2.0.
```sh
NUM="1.0";

NEWNUM=`echo ${NUM} | awk -F. -v OFS=. 'NF==1{print ++$NF}; NF>1{if(length($NF+1)>length($NF))$(NF-1)++; $NF=sprintf("%0*d", length($NF), ($NF+1)%(10^length($NF))); print}'`

echo "------" + $NEWNUM
```
#### Mac OS 显示和关闭隐藏文件的脚本，

```sh
defaults write com.apple.finder AppleShowAllFiles -bool true

killall Finder

defaults write com.apple.finder AppleShowAllFiles -bool false

```

### 删除找到的所有文件脚本，$1 需要搜索的文件夹，$2 需要删除的的文件名称

```sh
#!/bin/bash
##############################################

DIR=`echo "$1"`
echo "Target:$DIR"

OLDNAME=`echo "$2"`
echo "Filename:$OLDNAME"

find "$DIR" -name "$OLDNAME" | while read -r NAME

do
echo "remove: $NAME"

if [ -d "$NAME" ];then
    rm -rf "$NAME"
else
    if [ -e "$NAME" ];then
        rm -f "$NAME"
    fi
fi

done

```

### 音乐格式转换Mac OS 脚本
* Wav 文件转换为Caf音频文件

```sh
for f in *.wav; do
    echo "processing $f file...."
    afconvert -f caff -d LEI16@44100 -c 1 "$f" "${f/wav/caf}"
done

```

* Mp3 文件转换为Wav音频文件

```sh
for f in *.mp3; do
    echo "processing $f file...."
    afconvert -f WAVE -d LEI16@44100 -c 1 "$f" "${f/mp3/wav}"
done

```

* Mp3 文件转换为Caf音频文件

```sh
for f in *.mp3; do
    echo "processing $f file...."
    afconvert -f caff -d LEI16@44100 -c 1 "$f" "${f/mp3/caf}"
done

```

