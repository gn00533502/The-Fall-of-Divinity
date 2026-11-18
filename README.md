# 翻書小說網站

網頁會直接讀取 `novel.docx`，自動分頁並做成可以由右往左翻的書。

## 放上 GitHub

1. 在 GitHub 建立一個新的 Public repository。
2. 按 **Add file → Upload files**，上傳 `index.html`、`novel.docx`、`README.md`（續集檔也一起放在這一層），再按 **Commit changes**。
3. 到 **Settings → Pages**，Source 選 **Deploy from a branch**，Branch 選 **main**、資料夾選 **/(root)**，按 **Save**。
4. 等一兩分鐘，網址會顯示在同一頁，通常是 `https://你的帳號.github.io/repository名稱/`。

## 更新小說

- **修改第一個檔案**：在 Word 改好後，命名為 `novel.docx` 再上傳覆蓋。
- **接續新章節**：把第 6 章以後寫在新的 Word 檔，命名為 `novel-2.docx` 上傳；再下一批是 `novel-3.docx`，依此類推。編號不能跳號，網頁讀到缺號就會停止。
- **續集檔的開頭**：直接從 `CH VI` 這樣的章節標題開始。第一行也可以放書名，會自動略過。
- **修改舊章節**：如果後面的檔案出現同名章節（例如又有一個 `CH VI`），會以後面的內容為準。

## 閱覽次數

每次有人打開連結就加 1，同一個分頁重新整理不重複計算，你自己打開也算。數字顯示在封面和目錄視窗底部，資料存在免費的 [Abacus](https://v2.jasoncameron.dev/abacus) 計數服務；服務連不上時數字會隱藏，不影響閱讀。連續 6 個月無人造訪，計數可能到期。

不想使用時，把 `index.html` 裡的 `views: true` 改成 `views: false`。

## 書籤

看到想留的頁面按工具列的「書籤」，再按一次取消；所有書籤都列在「目錄」視窗裡。書籤存在讀者自己的瀏覽器，換裝置或清除瀏覽資料後不會保留。

## Word 的寫法

- 第一段是書名。
- 書名之後、第一章之前的文字會放在題記頁。
- 單獨一行的 `CH I`、`CH 2`、`第一章`、`第三回` 會被當成章節標題。
- 粗體會保留；空白行只用來分段，不會顯示成空行。

## 封面作者名

用文字編輯器打開 `index.html`，搜尋 `author`，把 `author: ''` 改成例如 `author: '你的筆名'`。

## 注意

免費版 GitHub Pages 需要 Public repository，任何人都能下載 `novel.docx`，檔案內容與 Word 檔的作者資訊也會一併公開。
