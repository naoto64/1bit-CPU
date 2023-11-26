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
<table>
  <thead>
    <tr>
      <th>命令</th>
      <th>機械語</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td>ADD A, Im</td>
        <td>0</td>
        <td>AレジスタにIm（イミディエイトデータ）を加算する。</td>
    </tr>
    <tr>
        <td>JMP Im</td>
        <td>1</td>
        <td>Imで指定した先の番地へジャンプする。</td>
    </tr>
  </tbody>
</table>

## プログラム例
Aレジスタに1を加算し続けるプログラム
```text:
ADD A, 1
JMP 0
```

Aレジスタに1を加算するだけのプログラム
```text:
ADD A, 1
JMP 1
```
何もしないプログラム
```text:
JMP 0
```

## 回路図
![回路図](./img/schematic.jpg)

## 実装図
![回路図](./img/implementation-diagram.jpg)
