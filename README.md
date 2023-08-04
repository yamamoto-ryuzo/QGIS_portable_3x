# このサイトは　https://github.com/pigreco/QGIS_portable_3x の日本語翻訳及び補完を兼ねています。
### QGIS LTR

　https://github.com/pigreco/QGIS_portable_3x が更新されない時、補完的に追加します。  

 [OSGeo4W64_3.28.9](https://drive.google.com/file/d/1wqYdv8Ynb-G9fN9fjP6WxIB7o66gwbfH/view?usp=sharing)

## Perché questo repository

Per tenere traccia di come realizzare una **versione Portable di QGIS 3.x** senza necessariamente aver installato il software.

## Che cosa è una versione Portable

Per applicazione portabile (o applicazione portatile; in inglese portable application) si intende un software applicativo che non necessita di installazione all’interno del sistema operativo su cui viene eseguito. Programmi di questo genere possono essere memorizzati su supporto rimovibile come cd-rom o memorie flash. 
Un’applicazione portabile può indistintamente essere eseguita su qualsiasi computer in cui si dispone di un sistema operativo compatibile con l’applicazione stessa. Il vantaggio per l’utente è quindi quello di poter utilizzare la medesima applicazione su macchine diverse mantenendo le impostazioni personalizzate nell’uso dell’applicazione. Un secondo vantaggio delle applicazioni portabili deriva dal fatto che non richiedendo installazione possono spesso essere eseguite anche in ambienti in cui non si dispone dei diritti di amministrazione sul sistema operativo. [Wikipedia](https://it.wikipedia.org/wiki/Applicazione_portabile).

## 作業手順

 1. 本家と違い、普通にインストールしたものをそのままポータブル版にします。;
 2. **OSGeo4W** フォルダを作成します。;
 3. **QGIS** WIN64/ をダウンロードします。;
<p align="center"> <a href="http://download.osgeo.org/qgis/" target="_blank"><img src="./imgs/img_01.png" width="400" title="dowload"></a>
</p>
 適宜目的の最新バージョンをダウンロード  

 ![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/7774c212-199e-486f-b60f-a6babe394262)  
 4. インストール実行

 ![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5504b88e-87e8-4760-87fb-0da0fdb7b83d)   
 5. インストール先を変更　C:\Program Files\QGIS 3.28.9\　から **C:\OSGeo4W64\qgis\\** へ    

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/d25b35cd-eae4-48ff-8a6d-7b2d92b72b3f)  
 6. `c:\windows\syswow64`にある`msvcp100.dll` `msvcr100.dll` ファイルを `C:\OSGeo4W64\qgis\apps\qgis-ltr\bin\`　にコピー  

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5eb8abd2-1e84-4277-8cdf-f691b905c4bd)  
 7. ファイルを移動した影響で　`C:\OSGeo4W64\qgis\bin\qgis-ltr-bin.env`　ファイルを削除

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/2e24d899-5c9b-4666-9b88-24ee87d5cc23)  
 9.[qgis-ltr-grass.bat](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/blob/master/qgis-ltr-grass.bat)を　`C:\OSGeo4W64`　へコピー  
 
![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/93223237-dcc3-4c2a-a47b-f79a47089194)  
 10. `C:\OSGeo4W64\qgis\bin\qgis-ltr.bat` を起動   
  もしくは、新規コンフィグを作成したい場合は `C:\OSGeo4W64\qgis-ltr-grass.bat` を起動  

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/29fd640f-b0ad-4f53-8c6d-684b0dda9f65)  

---
## Connessione al Web e i Plugin

Ho fatto dei test, la **portable** si connette alla rete senza problemi.

Per quanto riguarda i **plugin**: è possibile installarli, ma verrà creata una cartella **QGIS** nel percorso relativo al profilo utente `C:\Users\nomeUtente\AppData\Roaming\QGIS\QGIS3\profiles\default`

---

**Riferimenti:**

- Idea presa da [qui](https://www.youtube.com/watch?v=iWbB0WPn6rM)
- Blog post su [Pigrecoinfinito](https://pigrecoinfinito.wordpress.com/2019/02/26/creare-una-versione-portable-di-qgis-2-18-ltr/)

**DISCLAIMER**

Questa guida è stata realizzata e testata nel mio laptop e funziona bene, si connette al web. Non mi assumo nessuna responsabilità su eventuali incidenti di percorso!!!

<p align="center"> <a href="https://giphy.com/explore/free-gif" target="_blank"><img src="./imgs/giphy.gif" width="500" title="avvio QGIS"></a>
</p>
