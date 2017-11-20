---
ms.date: 2017-06-12
author: eslesar
ms.topic: conceptual
keywords: "a DSC, a powershell, a konfiguráció, a beállítása"
title: "A DSC WindowsProcess erőforrás"
ms.openlocfilehash: c34d3cb1d4d9b899b45fba7b4b148a7c977f5365
ms.sourcegitcommit: 75f70c7df01eea5e7a2c16f9a3ab1dd437a1f8fd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/12/2017
---
# <a name="dsc-windowsprocess-resource"></a>A DSC WindowsProcess erőforrás

> Vonatkozik: A Windows PowerShell 4.0-s verzióját, a Windows PowerShell 5.0

A **WindowsProcess** erőforrás a Windows PowerShell szükséges konfiguráló (DSC) folyamatok konfigurálása egy célcsomóponttal mechanizmust biztosít.

## <a name="syntax"></a>Szintaxis

```
WindowsProcess [string] #ResourceName
{
    Arguments = [string]
    Path = [string]
    [ Credential = [PSCredential] ]
    [ Ensure = [string] { Absent | Present }  ]
    [ DependsOn = [string[]] ]
    [ StandardErrorPath = [string] ]
    [ StandardInputPath = [string] ]
    [ StandardOutputPath = [string] ]
    [ WorkingDirectory = [string] ]
}
```

## <a name="properties"></a>Tulajdonságok
|  Tulajdonság  |  Leírás   | 
|---|---| 
| Argumentumok| Azt jelzi, a folyamat argumentumokat karakterlánc-értéke. Ha több argumentumot továbbítani kell, helyezze őket az összes ezt a karakterláncot.| 
| Elérési út| A folyamat végrehajtható fájl elérési útja. Ha ez a végrehajtható fájl (nem a teljes elérési útja), a DSC-erőforrás nevét átvizsgálja a környezet **elérési** változó (`$env:Path`) található a végrehajtható fájl. Ha ez a tulajdonság értéke egy teljesen minősített elérési útja, DSC nem fogja használni a **elérési** környezeti változót megtalálják a fájlt, és a rendszer hibaüzenetet küldjön, ha az elérési út nem létezik. Relatív útvonalak nem engedélyezettek.| 
| hitelesítő adatok| Azt jelzi, hogy a hitelesítő adatokat kell elindítania a telepítést.| 
| Győződjön meg arról| Azt jelzi, hogy létezik-e a folyamat. Állítsa be ezt a tulajdonságot "Elérhető" Győződjön meg arról, hogy létezik-e a folyamat. Egyéb esetben állítsa "Hiányzik". Az alapértelmezett érték az "Elérhető".| 
| dependsOn | Azt jelzi, hogy egy másik erőforrás konfigurációjának kell futtatni, mielőtt ehhez az erőforráshoz van konfigurálva. Például, ha az erőforrás-konfiguráció azonosítója blokk futtatni kívánt parancsfájl első az __ResourceName__ és annak típusa __ResourceType__, szintaxisa a következő e tulajdonság használatával "DependsOn ="[ A ResourceType] ResourceName"".| 
| StandardErrorPath| Azt jelzi, hogy a könyvtár elérési útja a normál hiba írni. Felülírja a meglévő fájlt.| 
| StandardInputPath| A szabványos bemeneti helyét jelöli.| 
| StandardOutputPath| Azt jelzi, hogy a helyet, ahova kiírhatná a normál a kimenetbe. Felülírja a meglévő fájlt.| 
| WorkingDirectory| Azt jelzi, hogy a helyet, a folyamat az aktuális munkakönyvtárban lesz.| 
