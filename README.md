# python_web_crawler(網頁爬蟲)

定義了三個網頁URL：url、urOn、urlNext，分別代表了Yahoo電影網站中的不同分類頁面，包括本週新片、上映中的電影和即將上映的電影。

定義了一個空的列表movies，用於存儲爬取的電影信息。

定義了一個名為crawl的函數，該函數接受一個URL作為參數，並爬取該URL中的電影信息。

在crawl函數內部，使用requests庫向指定的URL發送HTTP GET請求，然後使用BeautifulSoup庫對獲得的網頁內容進行解析。

使用BeautifulSoup找到網頁中所有包含電影信息的<div>元素，該元素的class為release_info_text，並遍歷這些元素。

對於每個電影信息，從中提取出中文名稱、英文名稱、上映日期和期待度等信息，然後將這些信息存儲到movies列表中。

最後，將movies列表轉換為Pandas DataFrame並命名各列，然後打印出結果。

最後，使用crawl函數分別爬取了三個不同URL（本週新片、上映中的電影、即將上映的電影）中的電影信息，並將結果以DataFrame的形式打印出來。

使用這段程式碼實現了網頁數據的爬取和整理，用於獲取Yahoo電影網站上的電影信息並進行展示。
