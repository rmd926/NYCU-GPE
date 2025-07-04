# 🔢 GPE 11028 - Digit Primes

![image](https://github.com/user-attachments/assets/d60a1deb-a3e6-443b-845c-b576d59d01ac)


## 題目說明
素數（Prime）是指大於 1、且恰好有兩個不同正因數的正整數。  
數位質數（Digit Prime）是指本身為質數，且其各位數字之和也是素數。例如：  
- 41 是數位質數，因為 4 + 1 = 5，而 5 是素數。  
- 17 不是數位質數，因為 1 + 7 = 8，而 8 不是素數。

給定多組查詢，每組查詢包含兩個整數 `t1` 和 `t2`，請求出區間 `[t1, t2]`（含端點）之間的數位質數個數。

## 輸入格式
第一行：整數 `N`，表示查詢組數，`0 < N ≤ 500000`  
接下來 `N` 行：每行兩個整數 `t1` 和 `t2`，滿足 `0 < t1 ≤ t2 < 1000000`

## 輸出格式
對於每一組查詢，輸出一行，一個整數，表示區間 `[t1, t2]` 內的數位質數數量。

## 範例
### 輸入
3
10 20
10 100
100 10000

### 輸出
1
10
576


## 解題提示
1. 使用 **埃拉托斯特尼篩法** 預先計算 `0` 到 `10^6` 間的所有質數。  
2. 實作函式計算整數的數位和，並判斷該數位和是否也是質數。  
3. 建立長度為 `10^6+1` 的 **前綴和** 陣列 `dp`，其中  dp[i] = 0..i 範圍內的數位質數總數
4. 對於每筆查詢 `[l, r]`，答案可由 dp[r] - dp[l-1] 在 O(1) 時間內取得。
5. 請使用快速 I/O（如 `sys.stdin.buffer` / `sys.stdout.write` 或 C++ 的 `scanf` / `printf`）以避免大量資料讀寫的效能瓶頸。  

