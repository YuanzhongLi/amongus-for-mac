# Among Usをmacでやる!
とうのは建前でmacにwindowsの環境を作ってやるだけです
### 1. VirtualBox
[ここ](https://pc-karuma.net/mac-virtualbox-install/)を参考にVirtualBoxをmacに入れよう

### 2. VirtualBoxでWindows10の環境を作る
#### 2-1. widonws10 isoのダウンロード
[ここ](https://www.microsoft.com/ja-jp/software-download/windows10ISO)からwindows10のISOをダウンロード  

エディションで**windows10**を選択して**確認**   
![エディション選択](img/2-1/select_edition.png)

言語は**日本語**を選択して**確認**  
![言語選択](img/2-1/select_language.png)

**64-bit**をダウンロード
![64bitダウンロード](img/2-1/download_64bit.png)

そうするとwindows10のisoのダウンロードが始まります.  
約5.3GBあるので多少時間かかるかもしれません.(僕は研究室のwifiでやったので1分くらいと爆速でした) 

#### 2-2. VirtualBoxにダウンロードさせたwindows10 isoをインストール
現在ダウンロードしたisoは`~/Downloads`下にあって`Win10_21H1_Japanese_x64.iso`の名称になっていると思います.  
これを`OS_iso`フォルダを作ってあげてそこにおいてあげましょう. 
terminalを開いて以下のように実行するとできます.  
~~~
cd
mkdir OS_iso
mv ~/Downloads/Win10_21H1_Japanese_x64.iso ~/OS_iso/
~~~

FinderでApplicationsを開いてVirtualBoxを開きましょう.  
![VirtualBoxを開く](img/2-2/applications_select_VirtualBox.png)
Among UsをやるたびにVirtualBoxを開く必要があるので,以下のようにdockにおいてあげると良いでしょう.
![VirtualBoxをDockにおく](img/2-2/keep_VirtualBox_in_dock.png)  

VirtualBoxを開くと以下のようなVirtualBoxのマネージャーのウィンドウが出てきます.  
**新規(N)** を選択しましょう.  
![VirtualBoxマネージャー](img/2-2/VirtualBox_manager.png)

以下のようなウィンドウが開くので,名前の部分をWindows10にしましょう.  
(自動でバージョンも変更されます.)  
![新しく作る](img/2-2/create_new.png)

次にRAMの割り当てがあるのですが、これは**8192MB(8GB)** 割り当てましょう.  
(無理な方は**4096MB** でも大丈夫だと思います.)  
![RAM](img/2-2/select_RAM_size.png)

ハードディスクの作成ではデフォルトの**仮想ハードディスクの作成する**を選びましょう.  
![ハードディスクの作成](img/2-2/virtual_harddisc.png)

ハードディスクのファイルタイプはデフォルトの**VDI**を選択しましょう.  
![VDI](img/2-2/select_VDI.png)

物理ハードディスクのあるストレージは,今回はAmong Usをやるのが目的でWindows10で色々とやる予定はないので固定サイズを選択します.  
![固定サイズ](img/2-2/select_fixed_size.png)

ファイルの場所とサイズではデフォルトのままで作成をしましょう.  
![ファイルの場所とサイズ](img/2-2/file_location_size.png)
作成中...  
![作成中](img/2-2/creating.png)
作成できました!  
![作成完了](img/2-2/creation_finish.png)

そしたら上画像にある**設定(S)** をクリックしましょう.  
以下のような画面になったら,**ストレージ**をクリックしましょう.  
![設定](img/2-2/open_settings.png)

以下のような画面になると思います.  
![ストレージ](img/2-2/select_storage.png)

以下のように**空**を選択して,その後**SATA ポート1**の隣にあるディスクアイコンから**ディスクファイルを選択**を選びましょう.  
![ディスクファイルを選択](img/2-2/select_discfile.png)

そしたら先ほどダウンロードしたwindows10のisoを選択しましょう.  
![isoを選択](img/2-2/select_iso.png)
選択したら以下のようになると思いますのでokを押しましょう.  
![iso選択完了](img/2-2/select_iso_finish.png)

以上で設定は終わりなので**起動**してあげましょう!  
![起動](img/2-2/boot.png)


#### 2-3. Widows10のセットアップ
起動するとこのような画面になります,基本的には指示に沿っていけば大丈夫です.  
![widons設定](img/2-3/setup.png)
ライセンスの認証というパートではラインセンスを購入して使用してもいいですが2万円くらいと高いです.  
なので今回はライセンスなしで行きます.  
ライセンスなしでも特に問題ないです.(ラインセンスについて知りたいなら[ここ](https://itojisan.xyz/%E3%83%91%E3%82%BD%E3%82%B3%E3%83%B3%E3%81%AE%E7%9F%A5%E8%AD%98/windows10%E3%81%AE%E3%83%A9%E3%82%A4%E3%82%BB%E3%83%B3%E3%82%B9%E8%AA%8D%E8%A8%BC%E3%81%97%E3%81%AA%E3%81%84%E3%81%A8%E3%81%A9%E3%81%86%E3%81%AA%E3%82%8B/))
以下のようにライセンスの画面になったら,**プロダクトキーがありません**を選択しましょう.  
![ライセンス](img/2-3/license.png)

OSは**Windows 10 Home**を選択しましょう.  
![OS](img/2-3/OS.png)
ライセンス条項に同意しましょう.  
![ライセンス同意](img/2-3/agree.png)

インストールの種類は下の方の**カスタム**を選びましょう.  
![インストール種類](img/2-3/select_install_type.png)

Windowsのインストール場所は以下のようにデフォルトのままで**次へ**行きましょう.  
![インストール場所](img/2-3/install_location.png)
Windowsインストール中...
![インストール中](img/2-3/installing.png)

インストールが完了したら再起動などもはさんで以下のようなアカウントを作成画面になります.  
Microsoftアカウントがある人はそれを使用してもいいですし,新しく作成でもいいと思います.  
ここまでお疲れ様でした,ようやくWindows10が使えます!  
![アカウント作成](img/2-3/account.png)

#### 2-4. 下準備
この章はカスタマイズについてなので,とばしても一応問題ないです. 

とりあえずChromeでもダウンロードしておきましょう.  
![ダウンロードChrome](img/2-4/download_Chrome.png)

ここでおそらくVirtualBoxでWindowsを使用している皆さんはVirtualBoxのウィンドウサイズを変更しても適用されない,macでコピーしたものがVirtualBoxでは機能しないなど不便を感じているかもしれません.  
それの解決方法を説明して行きます.  

### 3. Among Usを始めよう
#### 3-1. Steamのインストール
[ここ](https://zyoho3.com/?p=621)を参考にSteamをインストール
