# PopCatTW

一個連點工具

來幫台灣拿金牌吧~


# 怎麼做?
1. 複製 [Popcat.tw](#Popcattw-1) 的內容  ( 秘訣:點擊右上角的 ![copy](https://cdn.discordapp.com/attachments/805273033438134332/876873423769452645/Screenshot_2021-08-17_010044.png) 直接複製 ! )
2. 打開 Popcat 網站  (建議使用 Chrome 瀏覽器，不推薦使用 Safari )
    * **_強烈建議_**  打開網頁之後對著該分頁按下右鍵，並選擇 "[**關閉網站音訊(Chrome)** 或 **將索引標籤頁靜音(Edge)**](https://www.kocpc.com.tw/archives/197335 "如何快速讓電腦上的四大瀏覽器分頁靜音？ |  電腦王阿達")"
    * [Popcat 網站](https://popcat.click)
3. 按下鍵盤上的 `F12` 或 `Control(Ctrl)+Shift+i`  ( Mac 用戶請按下鍵盤上的 `Cmmand+Option+i` )
4. 在下方的 Console 中，貼上 [Popcat.tw](Popcat.tw) 的內容 [蛤? 我看不懂前面在說啥 . . .](#如何打開Console "如何打開 Console ?")
6. 按下 Enter 後，完成 ~
    * **_感謝你幫台灣出一份心力 \~_**
    * 這時，你可以去做別的事情，喝杯茶，寫寫作業，看個 YouTube 或滑一下 IG <!-- 如果都不想，打個手槍也行 --> ( 如果你看得到後面打什麼，記得幫我一下 <!-- 加 Discord 拜託 https://discord.gg/NzeAnxuRJn --> ฅ ^• ω •^ ฅ )


# Popcat.tw
複製起來 ~
```
(()=>{    
    console.clear()

    var event = new KeyboardEvent('keydown', {
	key: 'g',
	ctrlKey: true
});

setInterval(function(){
	for (i = 0; i < 100; i++) {
		document.dispatchEvent(event);
	}
}, 0);
    // Start sendStats interval
    document.dispatchEvent(event);
    // Total pops
    var total = 0;

    var iv = setInterval(()=>{
        // Get VUE
        var vue = document.getElementById('app').__vue__;
        // Check if user is marked as bot (just for safety measures, very unlikely to happen)
        if(vue.bot){
            console.log("%c You've been barked as a bot. Please clear your cookies.", "background: #a00; color: #fff");
            clearInterval(iv);
            return;
        }
        // Prevent ban
        vue.sequential_max_pops = 0;
        // Detect sendStats function run
        if(vue.accumulator == 0){
            total += 800;
            console.log(`[${new Date().toLocaleTimeString()}] %c800 pops sent (Total: ${total})`, "color: #0f0");
			// Open and close cat's mount
            vue.open = true;
            setTimeout(()=>{
                vue.open = false;
            }, 1000);
        }
        // Set 800 pops
        vue.accumulator = 800;
    }, 1000);

    console.log("%c Bot started. Waiting for the first request being sent. ", "background: #050; color: #0f0");
})();
```


# 如何打開Console?
https://cdn.discordapp.com/attachments/805273033438134332/876897555412303922/Edge.png
https://cdn.discordapp.com/attachments/805273033438134332/876897558650306590/Chrome.png
