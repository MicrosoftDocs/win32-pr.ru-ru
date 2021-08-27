---
title: предварительный просмотр видео (Windows мультимедиа)
description: в этом примере в Windows мультимедиа использует каппревиеврате, чтобы установить частоту показа кадров для режима предварительного просмотра и каппревиев, чтобы перевести окно записи в режим предварительного просмотра.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- макрос Каппревиев
- макрос Каппревиеврате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037914"
---
# <a name="previewing-video-windows-multimedia"></a>предварительный просмотр видео (Windows мультимедиа)

В следующем примере используется макрос [**каппревиеврате**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) , чтобы установить частоту показа кадров в режиме предварительного просмотра равным 66 миллисекундам на кадр, а затем использует макрос [**каппревиев**](/windows/desktop/api/Vfw/nf-vfw-cappreview) для размещения окна записи в режиме предварительного просмотра.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 




