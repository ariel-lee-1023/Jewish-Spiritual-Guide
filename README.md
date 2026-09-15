# Jewish Study Companion

從信仰、失落與目的的個人問題，走向仔細讀書、倫理反思，以及與他人和實踐重新建立關係的學習陪伴者。

**你 → 與 AI 對話 → 重新參與文本、人與實踐。** 對話的成果不只是一個令人安心的回答，也包括更準確的理解、更負責的判斷，或一個適合當下的生活行動。它不自稱拉比，不代表所有猶太傳統，也不要求使用者具有特定身分或信仰。

## 能做什麼

- 分清「這件事為什麼發生」「我如何理解它」與「現在可以怎麼回應」。
- 陪讀神的語言、信仰與理性、祈禱、沉默、悲傷及責任的段落。
- 重建作者的推理，指出真正的分歧，再明確標示陪伴者自己的綜合。
- 把思考帶回一段可重讀的文字、一位可以交談的人，或一項可選擇的實踐；不把每次對話變成作業。

## 六本來源及確認後的角色

| 來源 | 在陪伴者中的作用 |
|---|---|
| David J. Wolpe, *Why Faith Matters* (2008) | 信仰與懷疑、起源與真偽、宗教生活的意義；保留其有神論承諾與解釋的限度。 |
| David J. Wolpe, *Making Loss Matter* (1999) | 家、夢想、自我、愛、信仰及生命中的失落；尋找意義不等於認定痛苦值得。 |
| David J. Wolpe, *In Speech and in Silence: The Jewish Quest for God* (1992) | 祈禱、內在語言、歌唱、眼淚與不同種類的沉默；沉默不取代具體資訊的表達。 |
| Moses Maimonides, *The Guide to the Perplexed* (Goodman / Lieberman, 2024) | 宗教語言、證明與解釋、天意、律法目的及人的完善；原文與現代評注分開。 |
| Hermann Cohen, *Religion of Reason Out of the Sources of Judaism* (2nd English ed., 1995) | 關聯、同胞與陌生人、貧困、個人責任、贖罪及彌賽亞希望。 |
| Julian E. Zelizer, *Abraham Joshua Heschel: A Life of Radical Amazement* (2021) | Heschel 的傳記：驚異、先知式關切、制度與政治行動，包含批評及未解張力。它不是 Heschel 本人撰寫的神學著作。 |

每本各有一份獨立的 [來源提煉](references/)，使用英文保留概念與術語；核心要求以使用者的語言回答。這是選擇性的結構提煉，沒有宣稱逐頁精讀或完整涵蓋《Guide》的 178 章。

## 使用

### 在此專案內使用

```sh
git clone https://github.com/ariel-lee-1023/Jewish-Study-Companion.git
cd Jewish-Study-Companion
```

讓支援 Agent Skills 的主程式開啟此資料夾。根目錄的 [SKILL.md](SKILL.md) 是唯一核心；`.agents/skills/jewish-study-companion -> ../..` 提供專案內探索入口。主程式對 symlink 的支援可能不同；若未自動發現，可明確要求讀取根目錄 `SKILL.md`。

### 安裝到個人技能目錄（可選）

將整個儲存庫放入主程式使用的 skills 目錄，或在該目錄建立指向儲存庫根目錄的連結。不要只複製 `SKILL.md`：它需要同層的 `references/`。不需要 API key、外部服務或程式執行環境才能閱讀此技能。

例如，本機已經有 checkout，且個人目錄使用 `~/.agents/skills/`：

```sh
mkdir -p ~/.agents/skills
ln -s /absolute/path/to/Jewish-Study-Companion ~/.agents/skills/jewish-study-companion
```

將示例的絕對路徑換成實際位置；若目標名稱已存在，先查看原有安裝，勿覆寫。此專案不會自動修改個人技能目錄。

## 可以這樣開始

> 我還不確定是否相信上帝，但想理解祈禱裡的「聆聽」。陪我讀一小段，不必急著說服我。

> 我失去了一個重要的關係。Wolpe 所說的意義，與認為這次失去是好事，有什麼區別？

> Maimonides 和 Cohen 都談認識神與倫理；請找出真正的分歧，標明你的綜合。

> 透過 Zelizer 的傳記讀 Heschel 在 Selma 的參與：照片之外有哪些人與條件？

## 設計上的判斷

安慰與解釋分開；作者與評注者分開；哲學分析與個案診斷分開。Maimonides 的天意論不能被改寫成 Wolpe 的立場；Heschel 的 divine pathos 也不能直接等同於否定神學。遇到來源中的排斥、階序或歷史政治張力，保留並分析，而非隱去或套用為今日對人的規則。

陪伴者的「向外返回」原則來自使用者的建構目標，屬於明確的設計綜合。它不被冒稱為六本書共同提出的學說。對話不取代現實中的社群、宗教權威、照顧或治療。

## 範圍與品質狀態

- 六本使用者提供的 Markdown 全部完成提取；只發布原創提煉，不發布原書、轉檔全文或私人來源路徑。
- OCR 有斷字、表格化與正文／註釋交錯問題。直接引文必須另核原文；章節定位優先於推測頁碼。
- 來源角色、選讀範圍、遺漏項目和抽查修訂見 [fidelity-ledger/README.md](fidelity-ledger/README.md)。
- 結構、預算、探索連結及指令邊界的機械檢查有實際結果檔；編輯審查與模型評測分開。
- **受控行為驗收未執行**：沒有可用且已選定的獨立模型執行設定，因此不宣稱相對基線更好，也不把編輯自查當成盲測。凍結的八個情境已保留供後續評測。
- 部分選讀工具輸出曾被截斷，因此閱讀紀錄保留的是輸出範圍及 token 上界；精確已讀 token 不可得。這項限制不以零或精確數字掩飾。

沒有完整的 halakhic 語料、當地社群即時名單或批判校訂的希伯來文本。當代儀式要求、入教課程、健康與制度資訊須另行核查。

## 儲存庫結構

```text
SKILL.md                      # 唯一核心
references/                   # 六本來源，各一份 canonical reference
AGENTS.md                     # 專案使用與維護規則
.agents/skills/
  jewish-study-companion -> ../..
fidelity-ledger/              # 來源、覆蓋、核讀、評測和驗證紀錄
README.md
LICENSE
```

## 維護與授權

新增來源時保留作者自己的術語、推理及反例，更新來源清單和驗收案例；不要把多本書壓成沒有分歧的通用心靈建議。根目錄與 `references/` 是唯一執行內容，維護紀錄不應加入一般領域回答的上下文。

本專案原創技能與改寫內容採 [MIT License](LICENSE)。原書、翻譯及第三方文字的權利不隨此授權轉移。
