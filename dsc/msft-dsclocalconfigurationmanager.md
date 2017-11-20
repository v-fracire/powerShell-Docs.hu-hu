---
ms.date: 2017-06-12
author: eslesar
ms.topic: conceptual
keywords: "a DSC, a powershell, a konfiguráció, a beállítása"
title: "MSFT_DSCLocalConfigurationManager osztály"
ms.openlocfilehash: 35f732698fcc58f7bd43945edd10c143ffb79af9
ms.sourcegitcommit: 75f70c7df01eea5e7a2c16f9a3ab1dd437a1f8fd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/12/2017
---
# <a name="msftdsclocalconfigurationmanager-class"></a>MSFT_DSCLocalConfigurationManager osztály

A helyi Configuration Manager (LCM), amely a konfigurációs fájlok állapotát vezérli, és a konfigurációs ügynök használja a beállítások alkalmazásához.

A következő szintaxist az egyszerűsített Managed Object Format (MOF) kódból, és tartalmazza az összes örökölt tulajdonságait.

## <a name="syntax"></a>Szintaxis
------

``` syntax
[ClassVersion("1.0.0"), dynamic, provider("dsccore"), AMENDMENT]
class MSFT_DSCLocalConfigurationManager
{
};
```

## <a name="members"></a>Tagok
-------

A **MSFT_DSCLocalConfigurationManager** osztály a következő tagokkal rendelkezik:

-   [Módszerek] []

### <a name="methods"></a>Metódusok

A **MSFT_DSCLocalConfigurationManager** osztály rendelkezik, ezek a módszerek.

|Módszer |Leírás |
|:--- |:---|
| [ApplyConfiguration](msft-dsclocalconfigurationmanager-applyconfiguration.md)| A konfigurációs ügynök használja a beállítások, amelyek függőben van.| 
| [DisableDebugConfiguration](msft-dsclocalconfigurationmanager-disabledebugconfiguration.md)| Letiltja a DSC-erőforrás hibakeresés.| 
| [EnableDebugConfiguration](msft-dsclocalconfigurationmanager-enabledebugconfiguration.md)| A DSC-erőforrás hibakeresésének engedélyezése.| 
| [GetConfiguration](msft-dsclocalconfigurationmanager-getconfiguration.md)| A konfigurációs dokumentum küld a felügyelt csomóponthoz, és használja a **beolvasása** módszert a beállítások a konfigurációs ügynök.| 
| [GetConfigurationResultOutput](msft-dsclocalconfigurationmanager-getconfigurationresultoutput.md)| Egy adott feladat vonatkozó konfigurációs ügynök kimenetének beolvasása.| 
| [GetConfigurationStatus](msft-dsclocalconfigurationmanager-getconfigurationstatus.md)| A konfigurációs állapotának előzménye beolvasása.| 
| [GetMetaConfiguration](msft-dsclocalconfigurationmanager-getmetaconfiguration.md)| Lekérdezi a megadott konfigurációs ügynök szabályozzák, hogy LCM beállításokat.| 
| [PerformRequiredConfigurationChecks](msft-dsclocalconfigurationmanager-performrequiredconfigurationchecks.md)| A konzisztencia-ellenőrzés indítása.| 
| [RemoveConfiguration](msft-dsclocalconfigurationmanager-removeconfiguration.md)| Eltávolítja a konfigurációs fájlok.| 
| [ResourceGet](msft-dsclocalconfigurationmanager-resourceget.md)| Közvetlenül meghívja a **beolvasása** DSC erőforrás metódust.| 
| [Erőforráskészlete](msft-dsclocalconfigurationmanager-resourceset.md)| Közvetlenül meghívja a **beállítása** DSC erőforrás metódust.| 
| [ResourceTest](msft-dsclocalconfigurationmanager-resourcetest.md)| Közvetlenül meghívja a **teszt** DSC erőforrás metódust.| 
| [Visszaállítás](msft-dsclocalconfigurationmanager-rollback.md)| Vissza az előző konfigurációt összesíti.| 
| [SendConfiguration](msft-dsclocalconfigurationmanager-sendconfiguration.md)| A konfigurációs dokumentum küld a felügyelt csomóponthoz, és menti a függőben lévő módosítása.| 
| [SendConfigurationApply](msft-dsclocalconfigurationmanager-sendconfigurationapply.md)| A konfigurációs dokumentum küld a felügyelt csomóponthoz, és a konfigurációs ügynök segítségével a konfiguráció alkalmazásához.| 
| [SendConfigurationApplyAsync](msft-dsclocalconfigurationmanager-sendconfigurationapplyasync.md)| A konfigurációs dokumentum küldeni a felügyelt csomóponthoz, és indítsa el a beállítások a konfigurációs ügynök használatával. Használható GetConfigurationResultOutput eredmény kimeneti beolvasásához.| 
| [SendMetaConfigurationApply](msft-dsclocalconfigurationmanager-sendmetaconfigurationapply.md)| Beállítja a LCM beállítások konfigurációs ügynök használt.| 
| [StopConfiguration](msft-dsclocalconfigurationmanager-stopconfiguration.md)| A folyamatban lévő konfigurációs leáll.| 
| [TestConfiguration](msft-dsclocalconfigurationmanager-testconfiguration.md)| A konfigurációs dokumentum küld a felügyelt csomóponthoz, és a jelenlegi konfiguráció alapján a dokumentum ellenőrzi.| 



 

## <a name="requirements"></a>Követelmények
------------
>**MOF:** DscCore.mof

>**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration



 

 


