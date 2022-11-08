# OSI 模型與TCP/IP protocal suite

## OSI有七層?簡述其功能
- 7層分別為實體層、資料連結層、網路層、傳輸層、會議層、展示層及應用層
  - 實體層
    - 內容包含了纜線的規格、傳輸速度，以及資料傳輸的電壓值
  - 資料連結層
    - 資料連結層介於實體層與網路層之間，主要是在網路之間建立邏輯連結，並且在傳輸過程中處理流量控制及錯誤偵測，讓資料傳送與接收更穩定。
  - 網路層
    - 資料能夠在網路間傳遞。
  - 傳輸層
    - 可以將一個較大的資料切割成多個適合傳輸的資料，替模型頂端的第五、六、七等三個通訊層提供流量管制及錯誤控制。
  - 會議層
    - 負責建立網路連線，等到資料傳輸結束時，再將連線中斷，運作過程有點像召集多人開會（建立連線），然後彼此之間意見交換（資料傳輸），完成後，宣布散會（中斷連線）。
  - 展示層
    - 透過展示層可轉換表達方式，例如將ASCII編碼轉成應用層可以使用的資料，或是處理圖片及其他多媒體檔案，如JPGE圖片檔或MIDI音效檔。
  - 應用層
    - 功能是處理應用程式，進而提供使用者網路應用服務
    
## 底下網路設備運作在哪一層? Hub, switch, router, L4-switch, proxy
- Hub

## TCP/IP有哪些層?寫出與OSI七層模型的對應!
- 網路介面層，網路層，通道層，應用層 
- 網路存取層(Network Access Layer)，負責處理實體網路的一個介面，如：
   資料格式化、實體層的資料定址等。
 網際網路層(Internet Layer)，負責邏輯位址(即一般所用的IP位址)的資料傳輸。
 傳輸層(Transport Layer)，負責流程控制、錯誤檢查等。
 應用層(Application Layer)，負責一些應用的介面，如檔案傳輸、遠端控制等。
  - L1:Hub
  - L2:實體層Switch
  - L3:網路層router
  - L4:傳輸層
  - L7:應用層
## 簡述底下應用層協定(英文全名與簡單功能說明):
- HTTP vs HTTPs
  - HTTP
    - HyperText Transfer Protocol 超文本傳輸協定
    - HTTP是一種用於分佈式、協作式和超媒體訊息系統的應用層協定。
    - HTTP是全球資訊網的數據通信的基礎。
  - HTTPS
    - 常稱為HTTP over TLS、HTTP over SSL或HTTP Secure
    - HTTPS是一種透過計算機網路進行安全通訊的傳輸協定。
    - 利用SSL/TLS來加密封包。
    - HTTPS開發的主要目的，是提供對網站伺服器的身分認證，保護交換資料的隱私與完整性。
- DNS vs DNSsec
- telnet vs ssh
- ftp vs sftp
- smtp, pop3
- SNMP

## 簡述底下傳輸層協定(英文全名與簡單功能說明):TCP vs UDP
  - TCP
    - reliable(可靠的) vs unreliable(不可靠的)
    - TCP three-way handshaking(三項交握)
    - TCP syn flood attack
## 簡述底下網路層協定(英文全名與簡單功能說明): IP ICMP
- IP
- ICMP
