---
ms.date: 06/12/2017
keywords: DSC, powershell, a konfigurációt, a beállítása
title: Az MSFT_DSCLocalConfigurationManager osztály PerformRequiredConfigurationChecks metódusa
ms.openlocfilehash: b92eefb7fbea6d96afa31f6b802ba10fe20d4103
ms.sourcegitcommit: e04292a9c10de9a8391d529b7f7aa3753b362dbe
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/04/2019
ms.locfileid: "54048575"
---
# <a name="performrequiredconfigurationchecks-method-of-the-msftdsclocalconfigurationmanager-class"></a>Az MSFT_DSCLocalConfigurationManager osztály PerformRequiredConfigurationChecks metódusa

A Feladatütemező használatával egy konzisztencia-ellenőrzés indítása.

## <a name="syntax"></a>Szintaxis

```mof
uint32 PerformRequiredConfigurationChecks(
  [in] uint32 Flags
);
```

## <a name="parameters"></a>Paraméterek

*Jelölők* \[a\] bitmaszk, amely meghatározza a konzisztencia-ellenőrzés futtatásához. A következő értékek érvényesek, és a egy bitenkénti használatával egyesíthető **vagy** műveletet:

|Érték |Leírás |
|:--- |:---|
|**1** | Normál konzisztencia-ellenőrzést. |
|**2** | Újraindítás után konzisztencia-ellenőrzést folytatása. Ez az érték nem egyesíthetők más értékeket. |
|**4** | A megadott csomópont a metaconfiguration lekéréses kiszolgálón kell kéri le a konfigurációt. Ez az érték mindig kombinálni kell **1**, a egy értéke **5**. |
|**8** | A jelentéskészítő kiszolgáló állapota küldeni. |

## <a name="return-value"></a>Vrácená hodnota

Sikeres; a nulla értéket ad vissza egyéb esetben egy hibakódot ad vissza.

## <a name="remarks"></a>Megjegyzés

Ez a statická metoda.

## <a name="requirements"></a>Követelmények

**MOF:** DscCore.mof

**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration

## <a name="see-also"></a>Lásd még:

[**MSFT_DSCLocalConfigurationManager**](msft-dsclocalconfigurationmanager.md)