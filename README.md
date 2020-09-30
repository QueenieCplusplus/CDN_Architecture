# CDN_Architecture
CDN &amp; Peer 2 Peer



                           Central Node (Content Providers Server)
                           
                            /        \
                           /          \
                          /            \
                           
                      Area Node        Area Node
                      
                     /           |          \
                    /            |           \
                   /             |            \
                   
                Edge Node    Edge Node     Edge Node
 
               /                 |               \
              /                  |                \
             /                   |                 \
             
        Edge AS               Edge AS             Edge AS
        
          /
          
     enduser
     
     
  1. 客戶透過 EPG 伺服器向中央伺服器發出請求，中央伺服器經過認證確認後，根據使用者 IP 位址選擇一邊緣節點提供服務，並將該請求重新導向至該邊緣節點。
  
  2. 邊緣節點根據使用者請求內容，尋找使用者該內容的線上使用者節點清單，倘若命中，則根據排程策略，排程資源，並將參與服務的資源置為忙碌。
  
  3. 若不命中，則向上層或是鄰居邊緣節點請求內容，快取的同時，將該內容提供給使用者。
  
            
