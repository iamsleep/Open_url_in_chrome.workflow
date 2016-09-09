# Open_url_in_chrome.workflow

use Mac Automator and Service to improve working efficiency.
you can bind a hotkey from Mac keyboard -> service.

---
@ref chrome command list http://peter.sh/experiments/chromium-command-line-switches/

* Command line 下輸入
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --profile-directory=Profile\ 1 -url \0

* 結合 iterm2，讓符合 pattern url 可以在某個 user profile window 開啟頁面, 節省打密碼以及跑錯頁面的時間.

1. 打開 iterm profile
2. 選擇要修改的 profile name, 點選 Advanced
3. 看到 Smart Selection, 點選 Edit
4. 看到 Notes 那一欄, double click HTTP URL, 同時跳出視窗 Context Menu Items for Smart Selection Rule
5. 按左下角的 + , 點選 Action 欄位並選擇 Run Command, Parameter 設定成 /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --profile-directory=Profile\ 1 -url \0
   (\0 表示 match 的 url)
6. 儲存 ok.
7. 接下來任意點選 url 都會導去指定 user profile 的視窗了.
