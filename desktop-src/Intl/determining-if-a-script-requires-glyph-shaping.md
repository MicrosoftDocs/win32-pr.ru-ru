---
description: В следующем примере вызывается Скриптжетпропертиес, чтобы определить, требуется ли для сценария каждого из последующих последовательных элементов формирование глифов.
ms.assetid: 75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7
title: Определение, требует ли сценарий формирования глифов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9feadb1a82564fe03db6e03511449c7942b519ba7d63e5898b04d7b9c27cf2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068264"
---
# <a name="determining-if-a-script-requires-glyph-shaping"></a>Определение, требует ли сценарий формирования глифов

В следующем примере вызывается [**скриптжетпропертиес**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , чтобы определить, требуется ли для сценария каждого из последующих последовательных [элементов](uniscribe-glossary.md) формирование глифов.


```C++
const SCRIPT_PROPERTIES **g_ppScriptProperties;
int g_iMaxScript;

WCHAR *pwcInChars = L"Unicode string to itemize";
int cInChars = wcslen(pwcInChars);
const int cMaxItems = 20;
SCRIPT_ITEM si[cMaxItems + 1];
SCRIPT_ITEM *pItems = si;
int cItems;

ScriptGetProperties(&g_ppScriptProperties,
                    &g_iMaxScript);

HRESULT hResult = ScriptItemize(pwcInChars,
                                cInChars,
                                cMaxItems,
                                NULL,
                                NULL,
                                pItems,
                                &cItems);
if (hResult == 0) {
    for (int i=0; i<cItems; i++) {
        if (g_ppScriptProperties[pItems[i].a.eScript]->fComplex) {

            // Item [i] is complex script text
            // requiring glyph shaping.

        } else {

            // The text may be rendered legibly without using Uniscribe. 
            // However, Uniscribe may still be used as a means of accessing 
            // font typographic features. 
        }
    }
} else {
    // Handle the error.
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



