# 1bit CPU 組み立てキット

## 概要
4個のロジックICを使用した1bit CPUの組み立てキットです。

## スペック
<table>
  <thead>
    <tr>
      <th>項目</th>
      <th>スペック</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td>汎用レジスタ</td>
        <td>1bit x 1</td>
    </tr>
    <tr>
        <td>アドレス空間</td>
        <td>1bit</td>
    </tr>
    <tr>
        <td>ROM容量</td>
        <td>4bit</td>
    </tr>
    <tr>
        <td>命令セット</td>
        <td>ADD, JMP</td>
    </tr>
    <tr>
        <td>プログラムカウンタ</td>
        <td>1bit</td>
    </tr>
    <tr>
        <td>フラグレジスタ</td>
        <td>未実装</td>
    </tr>
    <tr>
        <td>算術演算</td>
        <td>1bitの加算（XOR）</td>
    </tr>
    <tr>
        <td>クロック周波数</td>
        <td>約1Hz</td>
    </tr>
    <tr>
        <td>IC総数</td>
        <td>4個</td>
    </tr>
  </tbody>
</table>

## 命令セット
|命令|機械語|説明|
|---|---|---|
|ADD A, Im|0|AレジスタにIm（イミディエイトデータ）を加算する。|
|JMP Im|1|Imで指定した先の番地へジャンプする。|

## プログラム例
### Aレジスタに1を加算し続けるプログラム
```text:
ADD A, 1
JMP 0
```

### Aレジスタに1を加算するだけのプログラム
```text:
ADD A, 1
JMP 1
```
### 何もしないプログラム
```text:
JMP 0
```

## 回路図
![回路図](./img/schematic.jpg)
