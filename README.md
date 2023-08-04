# 翻訳及び動作確認中

NOTA: A partire da QGIS 3.24 Tisler, gli eseguibili sono solo in formato `*.msi` e pesano circa 3 volte le vecchie `*.exe` perché contengono molti dati in più.
NOTA2: Il Plugin core **Geometry Checker** ha due [bug segnalati](https://lists.osgeo.org/pipermail/qgis-it-user/2023-April/010258.html) e risolti a partire da QGIS 3.28.6 e  QGIS 3.30.2

<!-- TOC -->

- [QGIS portable 3.x](#qgis-portable-3x)
  - [Perché questo repository](#perché-questo-repository)
  - [Che cosa è una versione Portable](#che-cosa-è-una-versione-portable)
  - [Step by step metodo manuale](#step-by-step-metodo-manuale)
  - [Step by step usando script Bash](#step-by-step-usando-script-bash)
  - [Connessione al Web e i Plugin](#connessione-al-web-e-i-plugin)
- [Portable (7z)](#portable-7z)
  - [OSGeo4W64 v2 - Nuovo Repository](#osgeo4w64-v2---nuovo-repository)
    - [QGIS](#qgis)
    - [QGIS LTR](#qgis-ltr)
  - [VECCHIO REPOSITORY OSGeo4W64 v1](#vecchio-repository-osgeo4w64-v1)
    - [Con GRASS GIS 7.8](#con-grass-gis-78)
    - [GRASS GIS non abilitato](#grass-gis-non-abilitato)

<!-- /TOC -->
# QGIS portable 3.x

Creare una versione **Portable di QGIS 3.x** usando il file `*.exe` scaricato dal sito http://download.osgeo.org/qgis/

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

11. ファイルを移動した影響で　C:\OSGeo4W\binqgis-ltr-bin.env　ファイルの　\QGIS32~1.9　を削除

![image](https://github.com/yamamoto-ryuzo/QGIS_portable_3x/assets/86514652/0fe4b328-b4a5-4bbc-aad9-097c99e088c6)

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


# Portable (7z)

## OSGeo4W64 v2 - Nuovo Repository
Con GRASS GIS 7.8, SAGA GIS 7.8.2, SpatiaLite 5, PDAL 2.2 - solo per win 10 64 bit

<p align="center"> <a href="" target="_blank"><img src="./imgs/qgis3280.png" width="700" title="info QGIS 3.22 LTR Białowieża"></a>

### QGIS LTR

CON GRASS 7.8.7 E SAGA 7.8.2

- ⭐⭐[QGIS 3.28.6-1 Firenze Portable](https://drive.google.com/file/d/10ZHR18Knf4fiHKN3L3qWSRO54f7FQi38/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.28.0-2`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐[QGIS 3.28.5-1 Firenze Portable](https://drive.google.com/file/d/10Vu-JFyuiiJcpwIjXaBkHIyG_Th28k1s/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.28.0-2`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐[QGIS 3.28.4-3 Firenze Portable](https://drive.google.com/file/d/108H_q4-pM40DMQB6cgUNxO2EfUkzn-Ws/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.28.0-2`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐⭐[QGIS 3.22.16-1 Białowieża Portable EOL](https://drive.google.com/file/d/103EBACERFZXL4IoNg3d0Q0FBaCu5sAcN/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐⭐[QGIS 3.22.15-1 Białowieża Portable EOL](https://drive.google.com/file/d/102IhVQRwTNu5T6d3Jv5Et_fZVBqyl6p1/view?usp=sharing) (**[HA UN grave BUG CONOSCIUTO](https://github.com/qgis/QGIS/pull/51703)**!!!) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐[QGIS 3.22.14-1 Białowieża Portable](https://drive.google.com/file/d/1-zzvZ5PjkBV4cTi1xXVYAMvfrfP8GeNC/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐⭐[QGIS 3.22.13-1 Białowieża Portable](https://drive.google.com/file/d/1-tdYRNtnFgWFsc2RNju5O1rnM6vOsXP7/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.12-1 Białowieża Portable](https://drive.google.com/file/d/1-pRs-0Mw-NiBNwGpeFYOjcJjP0vplT5C/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.11-1 Białowieża Portable](https://drive.google.com/file/d/1-i4mYs2F0HxhzRdHVKRW6ro-YhjadlYj/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.11-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- ⭐[QGIS 3.22.10-1 Białowieża Portable anche su Win7 64bit](https://drive.google.com/file/d/1-h381XZE2Eay4crHWPNQ3b7b1tQRQD4m/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.10-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.10-1 Białowieża Portable](https://drive.google.com/file/d/1-g_GH-JqsPqPRd-7mpn0NxmbF_nSy5z5/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.10-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.9-1 Białowieża Portable](https://drive.google.com/file/d/1-S272QXknZdWDbYcI2R9QBWo9pSNlUGI/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.9-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.8-1 Białowieża Portable](https://drive.google.com/file/d/1-ORu2NvPY0rgzddS9LTq03it-c_vSLZi/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.8-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.7-1 Białowieża Portable](https://drive.google.com/file/d/1RJzv6xL2iuL89YmQLIHzMYJnEW7EJtSa/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.7-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)
- [QGIS 3.22.6-1 Białowieża Portable](https://drive.google.com/file/d/1-AnZx7TxvP4JZr0er816Ex8ErbavLX1i/view?usp=sharing) (da unzippare in una pen drive (o dove preferite) `F:\OSGeo4W64-3.22.6-1`, doppio clic su `qgis-grass.bat`)(è una prima versione da testare, ogni suggerimento o segnalazione sono benvenute)(bug noti: <https://github.com/qgis/QGIS/issues/48380>)

**NB:**
- ⭐⭐⭐: EOL, ultimo rialscio
- ⭐⭐: occorre [rinominare](https://www.facebook.com/pigreco314/posts/pfbid02FAXfkezQXAU65SNzoX2Jq1nrn2jMeCz7w5jDktXbxG8in1ScJhCjL9x4aZsQ3yjml) il file `api-ms-win-core-path-l1-1-0.dll.w7` in `api-ms-win-core-path-l1-1-0.dll` (si trova nella cartella bin) per poterlo utilizzare in macchine che montano windows 7 64 b
- ⭐: utilizzabile anche in macchine che montano windows 7 64 bit

**DISCLAIMER**

Questa guida è stata realizzata e testata nel mio laptop e funziona bene, si connette al web. Non mi assumo nessuna responsabilità su eventuali incidenti di percorso!!!

<p align="center"> <a href="https://giphy.com/explore/free-gif" target="_blank"><img src="./imgs/giphy.gif" width="500" title="avvio QGIS"></a>
</p>
