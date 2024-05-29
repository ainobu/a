<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Q&A</title>
    <style>
        /* タブのスタイル */
        .tab {
            overflow: hidden;
            border: 1px solid #ccc;
            background-color: #f1f1f1;
        }
        .tab button {
            background-color: inherit;
            float: left;
            border: none;
            outline: none;
            cursor: pointer;
            padding: 14px 16px;
            transition: 0.3s;
            font-size: 17px;
        }
        .tab button:hover {
            background-color: #ddd;
        }
        .tab button.active {
            background-color: #ccc;
        }
        /* タブコンテンツのスタイル */
        .tabcontent {
            display: none;
            padding: 6px 12px;
            border: 1px solid #ccc;
            border-top: none;
        }
        /* サブメニューのスタイル */
        .submenu {
            display: none;
            padding: 6px 12px;
            border: 1px solid #ccc;
            border-top: none;
            background-color: #f9f9f9;
        }
        /* タブのグリッドレイアウト */
        .grid-container {
            display: grid;
            grid-template-columns: auto auto auto;
            gap: 10px;
        }
    </style>
</head>
<body>

<div class="grid-container">
    <button class="tablinks" onclick="toggleMenu(event, 'excel')">📝Excel</button>
    <button class="tablinks" onclick="toggleMenu(event, 'outlook')">📧Outlook</button>
    <button class="tablinks" onclick="toggleMenu(event, 'slack')">🍀Slack</button>
    <button class="tablinks" onclick="toggleMenu(event, 'nicollab')">📅Niコラボ</button>
    <button class="tablinks" onclick="toggleMenu(event, 'alladin')">📦アラジン</button>
    <button class="tablinks" onclick="toggleMenu(event, 'title')">タイトル</button>
    <button class="tablinks" onclick="toggleMenu(event, 'windows')">🌎Windows</button>
    <button class="tablinks" onclick="toggleMenu(event, 'other')">💊その他</button>
    <button class="tablinks" onclick="toggleMenu(event, 'search')">🔍詳細検索</button>
</div>

    <div id="excel" class="tabcontent">
      		<div class="qa-section">
            <div class="e">
            <b>Q: .xlsmファイルを開いたら、マクロの実行をブロックしたメッセージが表示される。</b>
			</div>
            <div class="answer">A:「インターネットオプション」の画面の「セキュリティ」タブで「信頼済みサイト」を
            選択して「サイト」ボタンをクリックし、「file://192.168.250.150」を追加する。
            (「このゾーンのサイトにはすべてサーバーの確認(https:)を必要とする」のチェックは外しておく)]
            </div>
            <details>
            <summary>備考</summary>
            <p>「詳細を表示」をクリックすると、ブラウザで下記のページが表示される。</p>
            <a href="https://support.microsoft.com/ja-jp/topic/%E6%BD%9C%E5%9C%A8%E7%9A%84%E3%81%AB%E5%8D%B1%E9%99%BA%E3%81%AA%E3%83%9E%E3%82%AF%E3%83%AD%E3%81%8C%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E3%81%95%E3%82%8C%E3%81%BE%E3%81%97%E3%81%9F-0952faa0-37e7-4316-b61d-5b5ed6024216">潜在的に危険なマクロがブロックされました - Microsoft サポート</a>
            </details>
		</div>
		<br>
        <div class="qa-section">
            <div class="question"><b>Q: セルにURLを入力すると、そのURLをクリックするとそのHPに飛ぶようになるが、HPに
            飛ぶようにしつつ文字を変更する方法はあるか。(例：<a href="http://google.com	">文字</a>や<a href="http://google.com">●</a>	など文字や記号に設定してリンクを飛ぶ方法)</b>
		</div>
            <div class="answer">A:HPに飛ぶ情報は「ハイパーリンク」という機能であり、それを変更しない限り
            文字を変更することは可能。そのセルをクリックすると画面が切り替わってしまうため、隣のセルを
            クリック(選択)して十字キーで編集したいセルに移動すると良い。</div>
        </div>
    </div>
	<div id="outlook" class="tabcontent">
		<div class="qa-section">
            <div class="question2">
            <b>Q:メールアプリを起動しようとすると、NewOutlookが起動する。</b>
			</div>
            <div class="answer">A:NewOutlookをアンインストール。
            </div>
            <details>
            <summary>備考</summary>
            <p><b>旧版起動</b></p>
            <a href="https://mitomoha.hatenablog.com/entry/2022/08/17/014118">Microsoft 365 新 Outlook から戻せなくなったら古い Outlook を直接開きましょう - （）のブログ</a>
            <p><b>画面から設定を戻す</b></p>
            <a href="https://too-support.my.site.com/faq/s/article/000003233">Outlook（16.6x〜）で予期せず「新しい Outlook」に変更されメールの閲覧や送受信ができなくなった</a>
            </details>
            <div class="question2">
            <b>Q:インポートしても人数分「名前がありません」が表示される</b>
			</div>
            <div class="answer">A:outlookのエクスポートファイル(.csv)はUTF-8で作成されるが、インポートする時はSJISで処理される。このため、.csvをSJISに変換してからインポートして、正常に処理された。</div>
            <details>
			<summary>備考</summary>
            <p>.pstによるエクスポート／インポートの機能もあるが、.csvより前に実行して失敗している。</p>
            </details>
            </div>
		</div>
	<div id="slack" class="tabcontent">
		<div class="qa-section">
            <div class="question3">
            <b>Q:マウスカーソルが表示されない。 </b>
			</div>
            <div class="answer">A:Windows再起動。
            </div>
            <details>
            <summary>備考</summary>
            <p>Slackのウィンドウの中ではマウスカーソルが表示されなくなった。タスクバーや、他のウィンドウでは表示される。</p>
            </details>
		</div>
    </div>

	<div id="nicollab" class="tabcontent">
		<div class="qa-section">
            <div class="question4">
            <b>Q: ワークフローのリストをダウンロードしたい。「一括操作」ではPDFしか出力出来ないが、Excelやcsvで出力したい。</b>
			</div>
            <div class="answer">A:「詳細検索」で「申請書類」を指定すると、「書き出し」ボタンが表示される。このボタンをクリックすると、csvで出力される。
            </div>
            <br>
            <div class="question4">
            <b>Q: 回覧板の選択項目を増やす方法が分からない。選択項目に「議事録」があるので追加ができるはずだが、どの画面で追加するかが分からない。</b>
			</div>
            <div class="answer">A:右側にある「その他」の欄は自由に入力することが出来、そこに入力して回覧板を作成すると、次回以降は選択項目に追加された状態になります。
            </div>
            <br>
            <div class="question4">
            <b>Q: 承認する時に通知設定にチェックを入れた状態で処理しようとすると、正しく処理されない場合がある。これを回避するため、通知設定を非表示または無効化したい。</b>
			</div>
            <div class="answer">A:通知設定を非表示または無効化することは出来ません。
            </div>
            <br>
            <div class="question4">
            <b>Q: 「コメント通知」ボタンをクリックしないと通知先が見えないが、デフォルトで選択されているため「完了」をクリックした時に意図せず通知してしまう。</b>
			</div>
            <div class="answer">A:デフォルトで選択なしには出来ません。
            </div>
		</div>
    </div>
	<div id="alladin" class="tabcontent">
		<div class="qa-section">
            <div class="question5">
            <b>Q:2重起動のメッセージが出て、起動できない</b>
			</div>
            <div class="answer">A:とりあええずの対応として、Alt+Tabで画面を表示して閉じていった。後で、PCを再起動したらサーバーのタスクバーは表示された。            </div>
            <details>
            <summary>備考</summary>
            <p>実際には最小化されていただけだと思われるが、このPC(本館2F左)はリモートデスクトップを使用した場合に、デスクトップはサーバー側だがタスクバーはクライアント側が表示されている。このため、最小化状態であることが分からず、2重起動をしていた。</p>
            </details>
		</div>
    </div>
	<div id="title2" class="tabcontent">
		<div class="qa-section">
            <div class="question6">
            <b>Q:e </b>
			</div>
            <div class="answer">A:
            </div>
            <details>
            <summary>備考</summary>
            <p></p>
            <a href="url">title</a>
            </details>
		</div>
    </div>
	<div id="windows" class="tabcontent">
		<div class="qa-section">
            <div class="question7">
            <b>Q: アドレス帳の編集が出来ない</b>
			</div>
            <div class="answer">A:「フォルダーの指定」で、デフォルトであるドキュメントの中の「Canon FAX Data」を選択したら、「このフォルダにはすでにアドレス帳データが存在します。このデータを使用しますか？」というメッセージが出たため、「はい」を選択したら復旧した。画面等については備考欄のURLを参照。
            </div>
            <details>
            <summary>備考</summary>
            <p><a href="https://faq.canon.jp/app/answers/detail/a_id/103956/~/%E3%80%90ir-adv%E3%80%91%E3%83%91%E3%82%BD%E3%82%B3%E3%83%B3%E3%81%8B%E3%82%89%E3%83%95%E3%82%A1%E3%82%AF%E3%82%B9%E9%80%81%E4%BF%A1%E6%99%82%E3%80%81%E3%82%A2%E3%83%89%E3%83%AC%E3%82%B9%E5%B8%B3%E3%81%8C%E6%B6%88%E3%81%88%E3%81%9F%EF%BC%8F%E3%80%8C%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%8C%E7%99%BA%E7%94%9F%E3%81%97%E3%81%9F%E3%81%9F%E3%82%81%E3%80%81%E3%82%A2%E3%83%89%E3%83%AC%E3%82%B9%E5%B8%B3%E3%82%92%E6%93%8D%E4%BD%9C%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%9B%E3%82%93%E3%81%A7%E3%81%97%E3%81%9F%E3%80%82%E3%80%8D%E3%81%AE%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%8C%E8%A1%A8%E7%A4%BA%E3%81%95%E3%82%8C%E3%81%9F%E3%81%A8%E3%81%8D%E3%81%AE%E5%AF%BE%E5%87%A6%E6%96%B9%E6%B3%95">【iR-ADV】パソコンからファクス送信時、アドレス帳が消えた／「エラーが発生したため、アドレス帳を操作できませんでした。」のエラーが表示されたときの対処方法</a></p>
            </details>
            <br>
            <div class="question7">
            <b>Q:リモートデスクトップで(アラジンで出力した.xlsxファイルを)コピーし、ローカルで貼り付けようとしても、無効(出来ない)状態になっている。
</b>
			</div>
            <div class="answer">A:リモート(サーバ)側でクリップボードを制御しているプロセスを再起動。(タスクマネージャーで「rdpclip.exe」を強制終了し、ファイルを指定して実行)
            </div>
            <details>
            <summary>備考</summary>
            <p>参照URLではグループポリシーの設定を変更する方法が記載されているが、アラジンのサーバーではグループポリシーを参照する権限が無いため、変更だけでなく確認も不可。
            <a href="https://atmarkit.itmedia.co.jp/ait/articles/1009/17/news125.html">【Windows 11対応】リモートデスクトップ接続でコピー＆ペーストする方法、できない場合の対処法：Tech TIPS - ＠IT</a></p>
            </details>
            <br>
            <div class="question7">
            <b>Q:アラジンのAPサーバに、パスワード入力なしでログイン出来ていたが、パスワードを求められるようになった。
</b>
			</div>
            <div class="answer">A:コマンドラインで下記を入力してEnter、メッセージが出るのでパスワードを入力。(IPアドレスとアカウントの番号部分は人によって異なる)
            <br>
            192.から始まるIPアドレスと、user;から始まるAlladinの数字2桁の部分が異なる
			Cmdkey /generic:TERMSRV/192.168.168.250.13 /user:TOYAKUAO\Aladdin56 /pass
            </div>
            <details>
            <summary>備考</summary>
            <p>Windows11のUpdateによって、資格情報の使用のデフォルト設定が変更されたために発生する現象。下記URL参照</p>
            <a href="https://blog.treedown.net/entry/2023/09/12/010000">Windows11のRDPはパスワード保存ができないので対処 - treedown’s Report</a></p>
            </details>
            <br>
            </div>
            <div class="question7">
            <b>Q:日刊薬業のPDFファイルがダウンロード出来なくなった。(他のExcelファイル等は出来る)</b>
            <div class="answer">A:プリンタに「Microsoft Print to PDF」を選択することで正常に保存出来る。
            </div>
            <details>
            <summary>備考</summary>
            <p>"未確認だが、ダウンロードフォルダには自動で保存されたファイルが残っているかも。(通信は正常に終了しているため)"</p>
            </details>
		</div>
    </div>
	<div id="other" class="tabcontent">
		<div class="qa-section">
            <div class="question8">
            <b>Q:プリンタのEPSON VP-D1800N(236)で納品書を印刷した場合、用紙が下から上へ送られるが、カバーの部分から上に行かない。</b>
			</div>
            <div class="answer">A:カバーについている歯車が本体の歯車とかみ合っておらず、ローラーが回転していなかった。カバーを一度外して再度取り付け、歯車が回るようになると、印刷も出来た。</div>
			<br>
		<div class="question8">
            <b>Q:ハンディスキャナのバーコードが読み込めない</b>
            <div class="answer">A:Windows Updateのための再起動が本館2F左のPC(ハンディの通信のサーバ)で実行されており、通信が出来ないために全ての機能が使えなくなっていたと思われる。</div>
       </div>
    </div>
    </div>

<div id="menu9" class="tabcontent">
    <h3>メニュー9</h3>
    <button onclick="openSubmenu('submenu9-1')">サブメニュー9-1</button>
    <button onclick="openSubmenu('submenu9-2')">サブメニュー9-2</button>
    <button onclick="openSubmenu('submenu9-3')">サブメニュー9-3</button>
    <div id="submenu9-1" class="submenu">サブメニュー9-1の内容</div>
    <div id="submenu9-2" class="submenu">サブメニュー9-2の内容</div>
    <div id="submenu9-3" class="submenu">サブメニュー9-3の内容</div>
</div>

<script>
    function toggleMenu(evt, pageName) {
        var i, tabcontent, tablinks;
        tabcontent = document.getElementsByClassName("tabcontent");
        tablinks = document.getElementsByClassName("tablinks");
        
        // Check if the clicked tab is already active
        var isActive = evt.currentTarget.classList.contains("active");
        
        // Hide all tab contents and remove active class from all tabs
        for (i = 0; i < tabcontent.length; i++) {
            tabcontent[i].style.display = "none";
        }
        for (i = 0; i < tablinks.length; i++) {
            tablinks[i].className = tablinks[i].className.replace(" active", "");
        }
        
        // If the clicked tab was not active, show its content and add active class
        if (!isActive) {
            document.getElementById(pageName).style.display = "block";
            evt.currentTarget.className += " active";
            
            // Hide all other tabs
            for (i = 0; i < tablinks.length; i++) {
                if (tablinks[i] !== evt.currentTarget) {
                    tablinks[i].style.display = "none";
                }
            }
        } else {
            // If the clicked tab was active, show all tabs again
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].style.display = "block";
            }
        }
    }

    function openSubmenu(submenuId) {
        var i, submenu;
        submenu = document.getElementsByClassName("submenu");
        for (i = 0; i < submenu.length; i++) {
            submenu[i].style.display = "none";
        }
        document.getElementById(submenuId).style.display = "block";
    }
</script>

</body>
</html>
