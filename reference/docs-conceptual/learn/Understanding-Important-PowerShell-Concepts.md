---
ms.date: 08/23/2018
keywords: PowerShell, a parancsmag
title: Fontos PowerShell fogalmainak megértése
ms.assetid: 3e601e38-4520-4578-a48d-b6779f1d35ee
ms.openlocfilehash: fad64563d1a7a6abd4f0e430331f81f91f43d312
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/14/2018
ms.locfileid: "53404140"
---
# <a name="understanding-important-powershell-concepts"></a>Fontos PowerShell fogalmainak megértése

A PowerShell-tervezési fogalmak számos különböző környezetekben történő integrálható. A fogalmak számos parancskörnyezet vagy programozási környezetben kezelőfelülettel személyek ismerős lesz. Azonban néhány személy fog tudni ezek mindegyike. Ezek a fogalmak némelyike megnézzük a rendszerhéj hasznos áttekintést nyújt.

## <a name="output-is-object-based"></a>Objektum alapú kimenete

Ellentétben a hagyományos parancssori felületen a PowerShell-parancsmagok objektumok kezelésére tervezték.
Egy objektum, amely több, mint a karakterlánc, a képernyőn megjelenő strukturált adatokat. A parancs kimenete mindig hajtja további információt, amelyet használhat, ha szüksége lesz rá.

Ha már használta a szöveg – a feldolgozás eszközök múltbeli adatok feldolgozásához, látni fogja, hogy azok eltérően viselkednek a PowerShell használatakor. A legtöbb esetben nem kell szöveg – a feldolgozás eszközök konkrét információk kinyeréséhez. Közvetlenül érheti el a PowerShell szabványos objektum-szintaxis használatával az adatok egyes részeit.

## <a name="the-command-family-is-extensible"></a>A parancs termékcsalád bővíthető

Felületek, például **cmd.exe** oly módon, hogy a beépített parancsa set közvetlenül kiterjesztése nem ad meg. Hozhat létre, amely a külső parancssori eszközök **cmd.exe**. De ezek külső eszközök nincs súgó integrációs szolgáltatások. **a Cmd.exe** automatikusan nem ismert, hogy a külső eszközök-e érvényes parancsokat.

A natív parancsokat a PowerShell nevezzük *parancsmagok* (ejtsd parancs-lehetővé teszi, hogy). Létrehozhat saját parancsmagok modulokat, és függvények használatával összeállított programkódban vagy szkriptekben. Modulok parancsmagok és szolgáltatók hozzáadhatja a rendszerhéjat. PowerShell is támogatja a parancsfájlokat, amelyek hasonló UNIX rendszerhéj-parancsfájlok és **cmd.exe** batch-fájlokat.

## <a name="powershell-handles-console-input-and-display"></a>PowerShell konzolon bemeneti és a megjelenített kezeli

A parancs beírásakor PowerShell mindig dolgozza fel a parancssori bemenet közvetlenül. PowerShell is formázza a kimenet a képernyőn látható. Ez a különbség azért fontos, mert csökkentik az egyes parancsmag szükséges munkát. Ez biztosítja, hogy mindig műveleteket végezheti el bármilyen parancsmaggal ugyanúgy. A parancsmag a fejlesztők nem kell elemezni a parancssori argumentumokat, vagy formázza a kimeneti kód írása.

A hagyományos parancssori eszközökkel rendelkezik saját rendszerek és a Súgó megjelenítése. Egyes parancssori eszközök használata **/?** a Súgó megjelenített; aktiválásához mások **-?**, **/H**, vagy akár **//**. Néhány súgó jelenik meg a grafikus felhasználói felület ablakban, és nem jelennek meg a konzolon. Használja a megfelelő paramétert, ha az eszköz előfordulhat, hogy hagyja figyelmen kívül mit írt be, és automatikusan a feladat végrehajtásának elindításához.
Mivel PowerShell automatikusan elemzi, és feldolgozza a parancssorban a **-?** paraméter mindig jelenti a "show me Súgó parancs".

> [!NOTE]
> Ha egy grafikus alkalmazást futtatja a PowerShell, az alkalmazás az ablak nyílik meg.
> PowerShell inkonzisztensek, csak ha feldolgozása a parancssori bemenet, ellátási vagy az alkalmazás kimenete a konzolablakban vissza. Hogyan működik az alkalmazás belső nincs hatással.

## <a name="powershell-uses-some-c-syntax"></a>PowerShell néhány C# szintaxisát használja.

PowerShell a .NET-keretrendszer épül. Egyes szintaxis szolgáltatások és a kulcsszavak azt megosztja a C# programozási nyelv. PowerShell megismeréséhez teheti, hogy sokkal könnyebben tanulhatja a C#. Ha már ismeri a C#, ezek Hasonlóságok teheti könnyebben PowerShell megismeréséhez.
