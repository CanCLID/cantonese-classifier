# 粵文分類器

呢個係個粵文分類器，會將輸入文本分成四類:

1. `cantonese`: 純粵文，僅含有粵語特徵字詞，例如“你喺邊度”
1. `mandarin`: 純官話文，僅含有官話特徵字詞，例如“這不對吧”
1. `mixed`：官粵混雜文，同時含有官話同粵語特徵嘅字詞，例如“是咁的”
1. `neutral`：無特徵漢語文，唔含有官話同粵語特徵，既可以當成粵文亦可以當成官話文，例如“去學校讀書”

分類方法係官話同粵語嘅特徵字詞識別。如果同時含有官話同粵語特徵詞彙就算官粵混雜，如果唔含有任何特徵，就算冇特徵中性文本。

## 使用方法

首先要有一個輸入文檔，例如`input.txt`，入面每一行係一個句子，然後運行下面命令

```bash
python3 main.py --input input.txt
```

輸出係一個 `output.tsv`，入面有分成兩列，第一列係判斷標籤，第二列係句子原文本。