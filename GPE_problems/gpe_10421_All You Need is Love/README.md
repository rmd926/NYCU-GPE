# 💖 GPE 10421 - All You Need Is Love
![image](https://github.com/user-attachments/assets/78faf673-d8cb-4b9e-bab9-4fe009e360fd)

![image](https://github.com/user-attachments/assets/464f4067-a81b-4bde-af7c-8d11d54ed2ef)


## 📘 題目敘述

一台名為「love machine」的裝置能判斷一組二進位字串是否是由另一組二進位字串唯一使用 0 和 1 所組成的。

給定兩組有效的二進位字串 \( S_1 \) 和 \( S_2 \)，判斷是否存在一組字串 \( L \)，使得 \( S_1 \) 和 \( S_2 \) 都只由 \( L \) 中的字元組成。  
這裡的減法定義為在二進位數字中以二進位基底相減，反覆減 \( L \) 直到等於 \( L \) 本身。

若存在符合條件的 \( L \)，輸出 `All you need is love!`，否則輸出 `Love is not all you need!`。

---

## 💡 解題提示（Hint）

- 檢查是否存在字串 \( L \) 僅包含 0 和 1，且 \( S_1 \) 和 \( S_2 \) 都僅由 \( L \) 的字元構成。
- 換句話說，\( L \) 是 \( S_1 \) 和 \( S_2 \) 中共同出現的 0 與 1 字元集合。
- 若 \( S_1 \) 和 \( S_2 \) 中 0 和 1 的集合交集不為空，即有共同字元，則可判定存在符合條件的 \( L \)。
- 注意字串的有效性與題目所述的限制條件。
- 對多組輸入進行判斷，並依序輸出結果。

