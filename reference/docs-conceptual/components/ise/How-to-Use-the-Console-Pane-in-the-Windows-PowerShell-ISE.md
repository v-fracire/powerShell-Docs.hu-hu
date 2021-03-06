---
ms.date: 06/05/2017
keywords: PowerShell, a parancsmag
title: A Konzol panel használata a Windows PowerShell ISE-ben
ms.assetid: 44d67705-87c7-4a69-a53e-6471fdebb757
ms.openlocfilehash: 5bbbdd3b1f0324ff1a4f2298459f58640c4dc9a6
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/14/2018
ms.locfileid: "53404464"
---
# <a name="how-to-use-the-console-pane-in-the-windows-powershell-ise"></a>A Konzol panel használata a Windows PowerShell ISE-ben

A konzol ablaktáblában található a Windows PowerShell integrált parancsfájlkezelési környezet (ISE) a Windows PowerShell ISE-t önálló konzolablakban hasonlóan működik.

Futtassa a parancsot a konzolablakban, írja be a parancsot, és nyomja le az ENTER BILLENTYŰT. Adja meg a feladatütemezési hajtsa végre a kívánt több parancsot, írja be a SHIFT + ENTER parancsok között. Lásd: [kiegészítés használata a parancsfájl panelen és a konzol ablaktáblában hogyan](How-to-Use-Tab-Completion-in-the-Script-Pane-and-Console-Pane.md) segítséget a parancsokat.

A parancs, az eszköztáron leállításához kattintson **leállítása műveletet**, vagy nyomja le a CTRL + BREAK billentyűkombinációt. CTRL + C használatával állítsa le a parancsot, ha a környezet egyértelmű. Például ha valamilyen szöveget a jelenlegi panelen van jelölve, majd CTRL + C hozzárendeli a másolási művelet.

Windows PowerShell v3 kezdve a Tesztkimenet ablaktáblán lett egyesítve a konzol ablaktáblában. Ez az előnye, hogy viselkedik, mint például az önálló Windows PowerShell-konzolt, és használata esetén nem volt szükség, ha a különálló eljárásokban közötti különbségeket. képes vagy:

- Válassza ki, és a konzol panelen szöveg másolása a vágólapra a Beillesztés bármely más ablakban. Szöveg kijelöléséhez kattintson, és tartsa az egérrel a tesztkimenet ablaktáblán, miközben az egérrel húzza a rögzíteni kívánt szöveg. Használhatja a kurzor nyílbillentyűk üzem közben **SHIFT** szöveg kijelöléséhez. Ezután nyomja le a CTRL + C billentyűt, vagy kattintson a **másolási** ikonra az eszköztárban.

- Illessze be a kijelölt szöveg, a jelenlegi kurzor pozíciójával. Kattintson a **beillesztési** ikonra az eszköztáron.

- A konzolablakban az összes szöveg törléséhez. A konzol ablaktáblában törléséhez kattintson a **konzol ablaktáblában törölje a jelet** ikonra az eszköztárban, vagy futtassa a parancsot a **Clear-gazdagépen** vagy az aliasával, **cls**.

## <a name="see-also"></a>Lásd még:

- [A Windows PowerShell ISE bemutatása](Introducing-the-Windows-PowerShell-ISE.md)