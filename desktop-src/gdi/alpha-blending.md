---
description: Альфа-смешение используется для вывода альфа-точечного рисунка, который является точечным рисунком с прозрачными или полупрозрачными пикселами.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Альфа-смешение (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985073"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="b24f1-103">Альфа-смешение (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="b24f1-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="b24f1-104">*Альфа-смешение* используется для вывода альфа-точечного рисунка, который является точечным рисунком с прозрачными или полупрозрачными пикселами.</span><span class="sxs-lookup"><span data-stu-id="b24f1-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="b24f1-105">В дополнение к красному, зеленому и синему каналу цвета каждый пиксель в альфа-изображении имеет компонент прозрачности, известный как *альфа-канал*.</span><span class="sxs-lookup"><span data-stu-id="b24f1-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="b24f1-106">Альфа-канал обычно содержит столько битов, сколько цветовой канал.</span><span class="sxs-lookup"><span data-stu-id="b24f1-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="b24f1-107">Например, 8-разрядный канал альфа может представлять 256 уровней прозрачности, от 0 (все растровое изображение прозрачно) до 255 (весь точечный рисунок непрозрачен).</span><span class="sxs-lookup"><span data-stu-id="b24f1-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="b24f1-108">Механизмы альфа-смешения вызываются путем вызова [**алфабленд**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), который ссылается на структуру [**блендфунктион**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="b24f1-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="b24f1-109">Альфа-значения на пиксель поддерживаются только для RGB в 32 бит/с \_ .</span><span class="sxs-lookup"><span data-stu-id="b24f1-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="b24f1-110">Эта формула определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b24f1-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="b24f1-111">Он представлен в памяти, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b24f1-111">This is represented in memory as shown in the following table.</span></span>



|       |       |       |       |
|-------|-------|-------|-------|
| <span data-ttu-id="b24f1-112">31:24</span><span class="sxs-lookup"><span data-stu-id="b24f1-112">31:24</span></span> | <span data-ttu-id="b24f1-113">23:16</span><span class="sxs-lookup"><span data-stu-id="b24f1-113">23:16</span></span> | <span data-ttu-id="b24f1-114">15:08</span><span class="sxs-lookup"><span data-stu-id="b24f1-114">15:08</span></span> | <span data-ttu-id="b24f1-115">07:00</span><span class="sxs-lookup"><span data-stu-id="b24f1-115">07:00</span></span> |
| <span data-ttu-id="b24f1-116">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="b24f1-116">Alpha</span></span> | <span data-ttu-id="b24f1-117">Красный</span><span class="sxs-lookup"><span data-stu-id="b24f1-117">Red</span></span>   | <span data-ttu-id="b24f1-118">Зеленый</span><span class="sxs-lookup"><span data-stu-id="b24f1-118">Green</span></span> | <span data-ttu-id="b24f1-119">Синий</span><span class="sxs-lookup"><span data-stu-id="b24f1-119">Blue</span></span>  |



 

<span data-ttu-id="b24f1-120">Точечные рисунки также могут отображаться с коэффициентом прозрачности, применяемым ко всему точечному рисунку.</span><span class="sxs-lookup"><span data-stu-id="b24f1-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="b24f1-121">Любой формат растрового изображения может быть отображен с глобальным константным альфа-значением путем установки **саурцеконстанталфа** в структуре [**блендфунктион**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="b24f1-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="b24f1-122">Значение глобальной константы Alpha имеет 256 уровней прозрачности, от 0 (весь точечный рисунок полностью прозрачен) до 255 (все растровое изображение полностью непрозрачно).</span><span class="sxs-lookup"><span data-stu-id="b24f1-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="b24f1-123">Значение глобальной константы Alpha сочетается с альфа-значением для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="b24f1-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="b24f1-124">Пример см. в разделе [альфа-смешение точечного рисунка](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="b24f1-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



