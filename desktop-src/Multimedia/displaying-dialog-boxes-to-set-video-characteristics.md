---
title: Отображение диалоговых окон для установки характеристик видео
description: Отображение диалоговых окон для установки характеристик видео
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- Структура КАПДРИВЕРКАПС
- макрос Капдривержеткапс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e6ebfa0f75f4bcec63a693636085f16c342e53761b2cb1e67a0e2536fa5cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144477"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Отображение диалоговых окон для установки характеристик видео

Каждый драйвер записи может предоставить до трех различных диалоговых окон, используемых для управления аспектами обработки разрядов и отслеживания видео. В следующем примере показано, как отобразить эти диалоговые окна. Перед отображением каждого диалогового окна в примере вызывается макрос [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) и проверяется Возвращаемая структура [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) , чтобы определить, может ли драйвер записи отобразить его.


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> <dt>

[**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




