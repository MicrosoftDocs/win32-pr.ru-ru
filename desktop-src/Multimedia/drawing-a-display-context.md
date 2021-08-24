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
ms.openlocfilehash: e0f10d533fff97064ba3c6a081a2f1d0aaa9e1b72011f2baa1ac3a6bd1a81d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678724"
---
# <a name="drawing-a-display-context"></a>Рисование контекста отображения

В следующем примере подготавливается контроллер домена Дравдиб с помощью функции [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) до отображения нескольких изображений в последовательности точечных рисунков.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Дравдиб](using-drawdib.md)
</dt> </dl>

 

 




