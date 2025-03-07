project名稱 : 門診查詢系統
==
# 運作流程
- line bot 圖文選單啟動查詢功能
- 使用者選取欲查詢地區和科別
- 發送訊息到伺服器開始進行爬蟲
- 爬蟲完的資訊整理後傳回line bot介面
# 技術細節 
- LINE bot : 使用官方提供的Messaging API把爬蟲的伺服器和line bot連結起來
- WebCrawling : 環境使用Anaconda Spyder，使用python編寫程式並使用Seleium套件進行爬蟲
- Ngrok : 可以把外界的請求轉發到本機指定的port，這邊做為測試用的暫時伺服器
# 困難 
- 網頁應用的debug比有編譯器的程式還要難debug，大部分只能靠不斷試錯和精演累積，有時候問chatgpt，也不見得有答案
- 要把爬蟲的訊息包裝成可顯示在line需要按照其格式，但是由於網路查的資料和gpt給的程式碼都不是最新的格式，最後是直接去找官方的github，根據第一手資料才修正成功。
- 原本有想要把此應用部屬到AWS Lambda上，但是因為未知錯誤加上時間緊迫所以就直接用Ngrok當作轉接的伺服器。
