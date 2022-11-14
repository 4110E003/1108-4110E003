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
    - 資料都是明文，傳遞的過程中有惡意竊聽者，資料便有機會被窺探、盜用。
  - HTTPS
    - 全名是 超文本傳輸協定， S 就是 Secure 的意思
    - 非對稱加密的運算量較高，傳遞回應較慢
    - 共用金鑰加密進行後續的傳遞，兼顧了安全性及傳遞速度。
- DNS vs DNSsec
  - DNS
    - 網域名稱系統
    - DNS 將網域名稱轉換為 IP 位址，以便瀏覽器能夠載入網際網路資源。
  - DNSsec
    - 網域名稱系統安全擴充（Domain Name System Security Extensions）
    - 一組加密密鑰對已發佈出去的 DNS 紀錄進行簽名，使紀錄更難以被偽造
- telnet vs ssh
  - telnet
    - 應用層協定，使用於網際網路及區域網中
    - 資料並未加密，帳號和密碼等敏感資料容易會被竊聽，因此很多伺服器都會封鎖Telnet服務，改用更安全的SSH
  - ssh
    - 安全外殼協定（Secure Shell Protocol）加密的網路傳輸協定，可在不安全的網路中為網路服務提供安全的傳輸環境
    - 最常見的用途是遠端登入系統，傳輸命令列介面和遠端執行命令
- ftp vs sftp
  - ftp
    - File Transfer Protocol (client and server)
    - 讓檔案從某部裝置傳遞至另一部裝置的軟體應用程式
  - sftp
    - Secure File Transfer Protocol，安全文件传输协议
    - 客户端与服务器间提供了一种更为安全的文件传输方式
- smtp, pop3
  - smtp
    - 主要用于系统之间的邮件信息传递，并提供有关来信的通知
  - pop3
    - Post Office Protocol - Version 3
    - 主要用于支持使用客户端远程管理在服务器上的电子邮件。提供了SSL加密的POP3协议被称为POP3S
- SNMP
  - 簡單網路管理協定（SNMP，Simple Network Management Protocol）
  - 協定能夠支援網路管理系統，用以監測連接到網路上的裝置是否有任何引起管理上關注的情況

## 簡述底下傳輸層協定(英文全名與簡單功能說明):TCP vs UDP
  - TCP
    - reliable(可靠的) vs unreliable(不可靠的)
    - TCP three-way handshaking(三項交握)
    - TCP syn flood attack
## 簡述底下網路層協定(英文全名與簡單功能說明): IP ICMP
  - IP
    - Internet Protocol Address
    - 網際協定中用於標識傳送或接收資料報的裝置的一串數字
  - ICMP
    - Internet Control Message Protocol
    - 網際網路協定（IP）中傳送控制訊息，提供可能發生在通訊環境中的各種問題回饋
