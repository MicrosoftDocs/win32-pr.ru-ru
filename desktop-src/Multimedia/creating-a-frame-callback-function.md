---
title: Создание функции обратного вызова Frame
description: Создание функции обратного вызова Frame
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- макрос Капсеткаллбакконфраме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b2a921bfae235c50387c41865c44bb69b5c05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329288"
---
# <a name="creating-a-frame-callback-function"></a><span data-ttu-id="c1872-104">Создание функции обратного вызова Frame</span><span class="sxs-lookup"><span data-stu-id="c1872-104">Creating a Frame Callback Function</span></span>

<span data-ttu-id="c1872-105">В следующем примере показана простая функция обратного вызова Frame.</span><span class="sxs-lookup"><span data-stu-id="c1872-105">The following example is a simple frame callback function.</span></span> <span data-ttu-id="c1872-106">Зарегистрируйте этот обратный вызов с помощью макроса [**капсеткаллбакконфраме**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="c1872-106">Register this callback by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```
TCHAR gachBuffer[100];  // Global buffer.
DWORD gdwFrameNum = 0;

// FrameCallbackProc: frame callback function. 
// hWnd:              capture window handle. 
// lpVHdr:            pointer to structure containing captured 
//                        frame information. 
// 
LRESULT PASCAL FrameCallbackProc(HWND hWnd, LPVIDEOHDR lpVHdr) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    _stprintf_s(gachBuffer, TEXT("Preview frame# %ld "), gdwFrameNum++); 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE ; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="c1872-107">См. также</span><span class="sxs-lookup"><span data-stu-id="c1872-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1872-108">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="c1872-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




