---
ms.date: 2017-06-12
contributor: manikb
ms.topic: reference
keywords: "gyűjtemény, a powershell, a parancsmag, a psget"
title: "Mentés-parancsfájl"
ms.openlocfilehash: 7b692d33e3f86a89505b8d37c0da4177f3dff2c2
ms.sourcegitcommit: 75f70c7df01eea5e7a2c16f9a3ab1dd437a1f8fd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/12/2017
---
# <a name="save-script"></a>Mentés-parancsfájl

Mentés-parancsfájl parancsmag lehetővé teszi, hogy tekintse át a parancsfájl által megadott helyre való mentése.

## <a name="description"></a>Leírás

A Save-parancsfájl parancsmag menti a rendszer a megadott parancsfájlt.

## <a name="cmdlet-syntax"></a>A parancsmag szintaxisa

```powershell
Get-Command -Name Save-Script -Module PowerShellGet -Syntax
```
## <a name="cmdlet-online-help-reference"></a>A parancsmag online Súgó-hivatkozás

[Mentés-parancsfájl](http://go.microsoft.com/fwlink/?LinkId=619786)

## <a name="example-commands"></a>Példa parancsok

### <a name="example-1-save-a-script-from-a-repository"></a>1. példa: Mentse a parancsfájlt a tárházból
Ez a parancs menti a parancsfájl Fabrikam-ClientScript GalleryINT tárházból a helyi mappába C:\ScriptSharingDemo legújabb verzióját

```powershell
Save-Script -Name Fabrikam-ClientScript -Repository GalleryINT -Path C:\ScriptSharingDemo
```

### <a name="example-2-save-a-version-of-a-script-by-piping-from-the-find-script-cmdlet"></a>2. példa: Egy parancsfájl verziója takaríthat meg a keresés-parancsfájl parancsmag átirányítás

Az első parancs megkeresi a Fabrikam-ClientScript a tárházból GalleryINT 1.5-ös verzióját, és menti a mappa C:\ScriptSharingDemo

A második parancs ellenőrzi a mentett parancsprogram-metaadatait.

```powershell
Find-Script -Name Fabrikam-ClientScript -Repository GalleryINT -RequiredVersion 1.5 | Save-Script -Path C:\\ScriptSharingDemo
Test-ScriptFileInfo C:\\ScriptSharingDemo\\Fabrikam-ClientScript.ps1

Version Name Author Description
------- ---- ------ -----------
1.5 Fabrikam-ClientScript manikb Description for the Fabrikam-ClientScript script
```
