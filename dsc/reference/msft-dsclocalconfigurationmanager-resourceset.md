---
ms.date: 06/12/2017
keywords: DSC, powershell, a konfigurációt, a beállítása
title: Az MSFT_DSCLocalConfigurationManager osztály ResourceSet metódusa
ms.openlocfilehash: 2712b7ff0a19e643c1f343d436c084f8970c9dd4
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/14/2018
ms.locfileid: "53404320"
---
# <a name="resourceset-method-of-the-msftdsclocalconfigurationmanager-class"></a>Az MSFT_DSCLocalConfigurationManager osztály ResourceSet metódusa

Közvetlenül meghívja a **beállítása** metódus a DSC-erőforrás.

## <a name="syntax"></a>Szintaxis

```mof
uint32 ResourceSet(
  [in]  string  ResourceType,
  [in]  string  ModuleName,
  [in]  uint8   resourceProperty[],
  [out] boolean RebootRequired
);
```

## <a name="parameters"></a>Paraméterek

*Erőforrástípus* \[a\] hívja az erőforrás nevét.

*ModuleName* \[a\] neve a modul, amely tartalmazza az erőforrás meghívásához.

*resourceProperty* \[a\] határozza meg az erőforrás-tulajdonság neve és értéke egy kivonattáblát a kulcs-érték, illetve. Használja a [Get-DscResource](/powershell/module/PSDesiredStateConfiguration/Get-DscResource) parancsmaggal a erőforrás-tulajdonságok és azok típusát.

*RebootRequired* \[ki\] a visszaadandó, ez a tulajdonság értéke **igaz** , ha a cél-csomópont újra kell indítani.

## <a name="return-value"></a>Vrácená hodnota

Sikeres; a nulla értéket ad vissza egyéb esetben egy hibakódot ad vissza.

## <a name="remarks"></a>Megjegyzések

Ez a statická metoda.

## <a name="requirements"></a>Követelmények

**MOF:** DscCore.mof

**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration

## <a name="see-also"></a>Lásd még:

[**MSFT_DSCLocalConfigurationManager**](msft-dsclocalconfigurationmanager.md)