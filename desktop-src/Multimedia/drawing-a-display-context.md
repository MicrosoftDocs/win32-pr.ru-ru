---
title: Рисование контекста отображения
description: Рисование контекста отображения
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- Дравдиб, контекст устройства (DC)
- Дравдиб, рисование контроллеров доменов
- Функция Дравдибреализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067942"
---
# <a name="drawing-a-display-context"></a><span data-ttu-id="95ca2-106">Рисование контекста отображения</span><span class="sxs-lookup"><span data-stu-id="95ca2-106">Drawing a Display Context</span></span>

<span data-ttu-id="95ca2-107">В следующем примере подготавливается контроллер домена Дравдиб с помощью функции [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) до отображения нескольких изображений в последовательности точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="95ca2-107">The following example prepares a DrawDib DC by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function prior to displaying several images in a bitmap sequence.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="95ca2-108">См. также</span><span class="sxs-lookup"><span data-stu-id="95ca2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95ca2-109">Использование Дравдиб</span><span class="sxs-lookup"><span data-stu-id="95ca2-109">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 




