# Chinpanish 翻訳ルール v1.5 （日本語｜中国語）

---

## 言語説明｜語言描述

**Chinpanish（チンパニッシュ）**は、日本語の語順と構文を保持しつつ、仮名のうち意味的に明確な要素を英語に置換し、漢字を原形のまま残すことで、**日本語話者と中国語話者の双方にとって意味解釈可能な中間表記体系（intermediate representation）として機能するよう設計された構造化転写形式である**。本規則文書は、**ChatGPT・Claude・Gemini などの大規模言語モデル（LLM）を基盤とした対話生成系 AI システムにおいて直接利用可能な形式であり、自然言語処理アルゴリズムに適した記述構造を持つ**。また、**日本語話者にとっても本形式は習得が容易であり、中国語話者との橋渡し的な意思伝達を迅速に実現できる**。

**Chinpanish**是一種保留日語語序與句法結構，將具備語義對應的假名轉換為英文詞彙，並保留漢字不變的結構化轉寫格式，**其設計目的是作為日語與漢語使用者之間可共同解讀的中介表述系統（intermediate representation）**。本規則文檔**可直接應用於 ChatGPT、Claude、Gemini 等基於大型語言模型（LLM）的對話生成系統中**，具備清晰語義對位、機器可讀性高、結構嚴謹等特性，**能有效支持自然語言處理任務中的輸出生成與交互理解**。

---

## 翻訳ルール一覧｜翻譯規則總覽

### 1. 漢字はそのまま保持（v1.0 追加）  
### 1. 保留漢字（v1.0 新增）

日本語文中に含まれるすべての漢字は**削除・翻訳・仮名化せず、そのまま残す**こと。  
所有日語中的漢字一律保留，不可轉為英文、刪除或改為假名。

**例：**  
明日は映画を見る → **明日 は 映画 watch**

---

### 2. 仮名（助詞・語尾）は英単語へ置換（v1.0 追加／v1.5 補強）  
### 2. 替換假名為英文（v1.0 新增 / v1.5 補強）

英単語と明確に対応する仮名（助詞や文末表現など）は**必ず英語に置換**すること。  
能夠明確對應英文的假名（助詞、語尾等）必須替換為簡單英文詞。

**例：**  
忘れずに受け取って → **忘 no に 受け取って**

---

### 3. 英訳できない仮名はそのまま保持（v1.0 追加）  
### 3. 無法對應的假名保留（v1.0 新增）

英訳が困難、または意味が不安定な仮名は**削除せずに原文のまま残す**。  
無法簡明翻譯成英文的假名（如語氣助詞、特殊語尾）保留原樣。

**例：**  
一緒に遊んでください → **一緒に 遊んで please**

---

### 4. 原文構成要素の削除は禁止（v1.5 追加）  
### 4. 不可刪除原文內容（v1.5 新增）

仮名・漢字を問わず、日本語原文のあらゆる要素を**削除してはならない**。  
無論是否替換，原文中任何成分皆不得刪除。

**誤：** 受け取って → ❌受 取  
**正：** → ✅受け取って

---

### 5. 数字はすべてアラビア数字に統一（v1.1 追加）  
### 5. 數字改為阿拉伯數字（v1.1 新增）

漢数字・仮名数詞は**アラビア数字に変換**し、単位（人・個・日など）は漢字で保持する。  
所有數字轉為阿拉伯數字，單位保留漢字不變。

**例：**  
三人で行く → **3人 with 行く**

---

### 6. 外来語（カタカナ）の処理（v1.4 修正）  
### 6. 外來語處理（片假名）（v1.4 修正）

カタカナ外来語の処理方法：  
a) 簡単な英語訳がある場合 → 英語に置換  
b) 難解または曖昧な語は → ローマ字表記に変換  
片假名外來語若能簡單對應英文即替換，否則轉寫為羅馬音。

**例：**  
テレビを見る → **TV watch**  
バンドエイドを貼る → **bandoeido stick**

---

### 7. 語順と句読点の保持（v1.3 追加）  
### 7. 語序與標點不可更動（v1.3 新增）

日本語原文の語順・句読点（、。）は**一切変更しない**こと。  
英文替換詞**必須原地對應原假名位置**，不能移動或換序。

**誤：** no 忘、受 取 please。❌  
**正：** 忘 no に 受け取って ✅

---

### 8. 分解置換は順序保持が前提（v1.5 追加）  
### 8. 可拆分替換但語序不可改（v1.5 新增）

「ずに」「たら」などの複合仮名は、漢字と英語の形に分解して置換可能だが、**語順は必ず原文通りに保つこと**。  
可拆分的假名結構可以轉換，但不得打亂原本語序。

**例：**  
忘れずに → ✅ 忘 no に  
❌ no 忘 に（語順違反）

---

## 使用上の注意｜使用提示

- Chinpanish は日本語の文意を中国語使用者が直接把握できるように最適化された補助的な表記形式である。  
  Chinpanish 是為了讓中文使用者更快理解日語句子的意思而設計的輔助型語法。  

- 主にチャット・字幕・AI対話・語学学習支援・音声翻訳・非公式文書などに適し、  
  正式な契約文書や教育資料では使用非推奨である。  
  本語法適用於聊天、字幕、語音翻譯、語言學習與非正式用語環境，**不建議用於正式文件與教育場景。**

---


# Chinpanish Translation Rules v1.5 (Japanese | English)

---

## Language Description

**Chinpanish** is a structured transliteration format that preserves Japanese word order and syntax, replaces semantically mappable kana components with English equivalents, and retains kanji in their original form. It is designed to function as an **intermediate representation jointly interpretable by both Japanese and Chinese users**.  
This specification is intended for direct use in **dialogue-generation systems based on large language models (LLMs)** such as ChatGPT, Claude, or Gemini. It features a structure well-suited for natural language processing tasks.

---

## Translation Rule List

### 1. Preserve all kanji (v1.0 added)

All kanji appearing in the Japanese sentence must be **retained without translation, deletion, or conversion to kana**.

**Example:**  
明日は映画を見る → **明日 は 映画 watch**

---

### 2. Replace kana (particles/endings) with English (v1.0 added / v1.5 enhanced)

All kana elements (especially particles or verb endings) that have a clear English equivalent **must be replaced with simple English words**.

**Example:**  
忘れずに受け取って → **忘 no に 受け取って**

---

### 3. Retain kana without English equivalents (v1.0 added)

If the kana element has no clear or consistent English equivalent (e.g., mood, nuance, or inflection), **it must be preserved as-is**.

**Example:**  
一緒に遊んでください → **一緒に 遊んで please**

---

### 4. Do not delete any original components (v1.5 added)

No kana or kanji may be deleted from the original Japanese sentence.  
**All original elements must remain**, regardless of whether they are replaced or not.

**Incorrect:** 受け取って → ❌受 取  
**Correct:** → ✅受け取って

---

### 5. Convert all numbers to Arabic numerals (v1.1 added)

Any numerical expressions written in kanji or kana must be **converted to Arabic numerals**, while units such as 人 (person), 個 (item), or 日 (day) are kept in kanji.

**Example:**  
三人で行く → **3人 with 行く**

---

### 6. Handle katakana loanwords (v1.4 revised)

For katakana loanwords:  
a) If there is a clear and common English equivalent → replace with English  
b) If rare or ambiguous → convert to romaji (romanized form)

**Examples:**  
テレビを見る → **TV watch**  
バンドエイドを貼る → **bandoeido stick**

---

### 7. Maintain original word order and punctuation (v1.3 added)

The original Japanese word order and punctuation (such as 、 and 。) **must not be altered**.  
Each English replacement must **appear in the same position as the kana it replaces**.

**Incorrect:** no 忘、受 取 please。❌  
**Correct:** 忘 no に 受け取って ✅

---

### 8. Split replacements are allowed but must preserve order (v1.5 added)

Compound kana elements (e.g., ずに, たら) may be **split into parts** and replaced, but **the original order must be maintained**.

**Example:**  
忘れずに → ✅ 忘 no に  
❌ no 忘 に (order violation)

---

## Usage Notes

- Chinpanish is an auxiliary representation format optimized to allow **Chinese users to directly comprehend the semantic content of Japanese sentences**.

- It is best suited for applications such as chat interfaces, subtitles, AI dialogue generation, language learning assistance, voice translation, and informal documentation.  
  **It is not recommended for use in legal documents, official publications, or formal education settings.**

---