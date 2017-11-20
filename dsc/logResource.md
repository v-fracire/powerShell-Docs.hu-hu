---
ms.date: 2017-06-12
author: eslesar
ms.topic: conceptual
keywords: "a DSC, a powershell, a konfiguráció, a beállítása"
title: "A DSC-napló erőforrás"
ms.openlocfilehash: 72c9c5a9b8e2a4ed4ce43cfd792572ce95b502b3
ms.sourcegitcommit: 75f70c7df01eea5e7a2c16f9a3ab1dd437a1f8fd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/12/2017
---
# <a name="dsc-log-resource"></a>A DSC-napló erőforrás 

> Vonatkozik: A Windows PowerShell 4.0-s verzióját, a Windows PowerShell 5.0

A __napló__ erőforrás a Windows PowerShell szükséges konfiguráló (DSC) üzeneteket írni a Microsoft-Windows-kívánt állapot konfigurációs/elemzési Eseménynapló mechanizmust biztosít.

```
Syntax

Log [string] #ResourceName
{
    Message = [string]
    [ DependsOn = [string[]] ]
}
```

Megjegyzés: Alapértelmezés szerint csak a műveleti naplókat DSC engedélyezve van.
Mielőtt a elemzési naplóját lesznek elérhetők, engedélyezni kell.
Tekintse meg a következő cikket.

[Hol találhatók a DSC-eseménynaplók?](https://msdn.microsoft.com/en-us/powershell/dsc/troubleshooting#where-are-dsc-event-logs)

## <a name="properties"></a>Tulajdonságok
|  Tulajdonság  |  Leírás   | 
|---|---| 
| Üzenet| Azt jelzi, hogy a konfiguráció/elemzési Microsoft-Windows-Desired állapot eseménynaplójába írhatja kívánt üzenetet.| 
| dependsOn | Azt jelzi, hogy egy másik erőforrás konfigurációjának kell futtatni, a napló üzenet beolvasása előtt. Például, ha az erőforrás-konfiguráció azonosítója blokk futtatni kívánt parancsfájl első az __ResourceName__ és annak típusa __ResourceType__, az e tulajdonság használatával szintaxisa a következő `DependsOn = "[ResourceType]ResourceName"`.| 

## <a name="example"></a>Példa

A következő példa bemutatja, hogyan üzenet tartalmazza a Microsoft-Windows-Desired állapot konfigurációs/elemzési eseménynaplójában.

> **Megjegyzés:**: futtatásakor [teszt-DscConfiguration](https://technet.microsoft.com/en-us/library/dn407382.aspx) az ehhez az erőforráshoz konfigurált, akkor a rendszer mindig visszaküldi **$false**.

```powershell 
Configuration logResourceTest
{
    Import-DscResource -ModuleName PSDesiredStateConfiguration

    Node localhost

    {
        Log LogExample
        {
            Message = "This message will appear in the Microsoft-Windows-Desired State Configuration/Analytic event log."
        }
    }
}
```
