---
title: Анимация палитры
description: Анимация палитры
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- Дравдиб, палитры
- Функция Дравдибреализе
- Функция Дравдибдрав
- Функция Дравдибчанжепалетте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791196"
---
# <a name="animating-a-palette"></a><span data-ttu-id="503bc-107">Анимация палитры</span><span class="sxs-lookup"><span data-stu-id="503bc-107">Animating a Palette</span></span>

<span data-ttu-id="503bc-108">В следующем примере палитра анимируется с помощью функций [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**дравдибчанжепалетте**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)и [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="503bc-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="503bc-109">Цвета точечного рисунка можно изменить с помощью функции [**дравдиббегин**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) в сочетании с [**дравдибчанжепалетте**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span><span class="sxs-lookup"><span data-stu-id="503bc-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="503bc-110">Во – первых, чтобы разрешить изменение палитры, укажите \_ флаг анимации DDF в вызове **дравдиббегин**.</span><span class="sxs-lookup"><span data-stu-id="503bc-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="503bc-111">Во вторых, задайте значения цветовой таблицы из записей палитры с помощью **дравдибчанжепалетте**.</span><span class="sxs-lookup"><span data-stu-id="503bc-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="503bc-112">Например, если *лппе* является адресом массива [палеттинтри](/previous-versions//ms532623(v=vs.85)) , содержащего новые цвета, а *лпби* является структурой [**Битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , используемой в [**ДРАВДИББЕГИН**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) или [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), следующий фрагмент обновляет таблицу цветов DIB.</span><span class="sxs-lookup"><span data-stu-id="503bc-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="503bc-113">См. также</span><span class="sxs-lookup"><span data-stu-id="503bc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="503bc-114">Использование Дравдиб</span><span class="sxs-lookup"><span data-stu-id="503bc-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 