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

4. インストール実行;
   
![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5504b88e-87e8-4760-87fb-0da0fdb7b83d)

6. インストール先を変更　C:\Program Files\QGIS 3.28.9\　から **C:\OSGeo4W\QGIS 3.28.9\\** へ;

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/d25b35cd-eae4-48ff-8a6d-7b2d92b72b3f)

7. ファルダの移動　C:\OSGeo4W\QGIS 3.28.9　以下のフォルダを　C:\OSGeo4W　へ

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/0e89b01d-e7bf-4612-98e5-18742f5a816a)
![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/672967ce-38f8-46be-a70c-cff7e9a3a481)

10. `c:\windows\syswow64`にある`msvcp100.dll` `msvcr100.dll` ファイルを `C:\OSGeo4W\apps\qgis-ltr\bin\`　にコピー

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/5eb8abd2-1e84-4277-8cdf-f691b905c4bd)

11. ファイルを移動した影響で　C:\OSGeo4W\binqgis-ltr-bin.env　ファイルを削除

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/2e24d899-5c9b-4666-9b88-24ee87d5cc23)

12. `C:\OSGeo4W\bin\qgis-ltr.bat` を起動

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/29fd640f-b0ad-4f53-8c6d-684b0dda9f65)

## Step by step usando script Bash

1. creare una cartella sul desktop `zanzibar`(oppure dove preferite);
2. scaricare il file [script.sh](./script.sh) all'interno della cartella `zanzibar` creata al punto 1;
3. avviare `Bash` e digitare `chmod +x ./script.sh` per i permessi e poi `./script.sh`;
4. dopo circa **30 minuti** otterrete una cartella zippata `OSGeo4W_349` con la versione portable di QGIS.
5. unzippate la cartella `OSGeo4W_349.7z` dove desiderate e avvire il file `qgis-ltr.bat` che trovate in `/OSGeo4W/bin`.

**PS:** nello script scarico la `QGIS-OSGeo4W-3.4.9-1-Setup-x86_64.exe` e i file `msvcp100.dll` `msvcr100.dll` versione a 64 bit!!!

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
