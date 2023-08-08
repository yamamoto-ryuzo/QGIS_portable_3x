# このサイトは　https://github.com/pigreco/QGIS_portable_3x の日本語翻訳及び補完を兼ねています。
# This site serves as a Japanese translation and supplement to https://github.com/pigreco/QGIS_portable_3x.
### QGIS LTR
　Complementary addition when https://github.com/pigreco/QGIS_portable_3x is not updated.  
　https://github.com/pigreco/QGIS_portable_3x が更新されない時、補完的に追加します。  

  - 2023-08-05 [OSGeo4W64_3.28.9-ltr_grass-saga.7z](https://drive.google.com/file/d/1wwvgiMAeqiw3pDRCRNT3OlMu_-zWWb7L/view?usp=sharing)  

## このリポジトリについて

 QGIS 3.xをインストールすることなく、動作することのできるポータブル版を作成する方法を説明します。  

## ポータブル版とは何か

ポータブル・アプリケーション（またはポータブル・アプリケーション）とは、実行するオペレーティング・システム内にインストールする必要のないアプリケーション・ソフトウェアを指す。  
この種のプログラムは、CD-ROMやフラッシュメモリなどのリムーバブルメディアに保存することができます。  
ポータブル・アプリケーションは、そのアプリケーションと互換性のあるオペレーティング・システムを搭載していれば、どのコンピューターでも無差別に実行することができます。  
**ユーザーにとっての利点は、アプリケーションの使用時にカスタマイズされた設定を維持しながら、異なるマシン上で同じアプリケーションを使用できることです。**  
ポータブルアプリケーションの第二の利点は、インストールを必要としないため、オペレーティングシステムの管理者権限を持っていない環境でも実行できます。 [Wikipedia](https://it.wikipedia.org/wiki/Applicazione_portabile).

## 作業手順

 1. 本家と違い、普通にインストールしたものをそのままポータブル版にします。;
 2. **QGIS** WIN64/ をダウンロードします。;
<p align="center"> <a href="http://download.osgeo.org/qgis/" target="_blank"><img src="./imgs/img_01.png" width="400" title="dowload"></a>
</p>
 適宜目的の最新バージョンをダウンロード  

 ![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/7774c212-199e-486f-b60f-a6babe394262)  
 3. インストール実行

 ![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5504b88e-87e8-4760-87fb-0da0fdb7b83d)   
 4. インストール先を変更　C:\Program Files\QGIS 3.28.9\　から **C:\OSGeo4W64\qgis\\** へ    

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/d25b35cd-eae4-48ff-8a6d-7b2d92b72b3f)  
 5. `c:\windows\syswow64`にある`msvcp100.dll` `msvcr100.dll` ファイルを `C:\OSGeo4W64\qgis\apps\qgis-ltr\bin\`　にコピー  

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5eb8abd2-1e84-4277-8cdf-f691b905c4bd)  
 6. ファイルを移動した影響で　`C:\OSGeo4W64\qgis\bin\qgis-ltr-bin.env`　ファイルを削除

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/2e24d899-5c9b-4666-9b88-24ee87d5cc23)  
 7.[qgis-ltr-grass.bat](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/blob/master/qgis-ltr-grass.bat)を　`C:\OSGeo4W64`　へコピー  
 
![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/93223237-dcc3-4c2a-a47b-f79a47089194)  
 8. `C:\OSGeo4W64\qgis\bin\qgis-ltr.bat` を起動   
  もしくは、新規コンフィグを作成したい場合は `C:\OSGeo4W64\qgis-ltr-grass.bat` を起動  

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/29fd640f-b0ad-4f53-8c6d-684b0dda9f65)  

 9.OSGeo4W64_3.28.9-ltr_grass-saga.7z に圧縮、バージョンを適宜変更

---
## ウェブ接続とプラグイン

**ポータブル版：** 何の問題もなくWEBに接続できます。

**プラグインについて：** インストールは可能ですが、ユーザープロファイルのパスに **QGIS** フォルダが作成されます。 `C:\Users\nomeUtente\AppData\Roaming\QGIS\QGIS3\profiles\default`

---

**参考資料**

- アイデア提供 [qui](https://www.youtube.com/watch?v=iWbB0WPn6rM)
- ブログ記事 [Pigrecoinfinito](https://pigrecoinfinito.wordpress.com/2019/02/26/creare-una-versione-portable-di-qgis-2-18-ltr/)

**免責事項**

このガイドは私のパソコンで作成され、テストされたものです。どんな災難にも責任は負いません！

<p align="center"> <a href="https://giphy.com/explore/free-gif" target="_blank"><img src="./imgs/giphy.gif" width="500" title="avvio QGIS"></a>
</p>
