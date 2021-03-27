---
description: В Windows GDI+ цвет — это 32-разрядное значение с 8 битами на каждый для альфа-, красного, зеленого и синего цветов.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Альфа-смешение цвета для линий и заливок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908903"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="9e069-103">Альфа-смешение цвета для линий и заливок</span><span class="sxs-lookup"><span data-stu-id="9e069-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="9e069-104">В Windows GDI+ цвет — это 32-разрядное значение с 8 битами на каждый для альфа-, красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="9e069-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="9e069-105">Альфа-значение обозначает прозрачность цвета — степень, до которой смешивается цвет с цветом фона.</span><span class="sxs-lookup"><span data-stu-id="9e069-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="9e069-106">Значения альфа находятся в диапазоне от 0 до 255, где 0 представляет полностью прозрачный цвет, а 255 — полностью непрозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="9e069-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="9e069-107">Альфа-смешение — это попиксельное смешение данных исходного и фонового цветов.</span><span class="sxs-lookup"><span data-stu-id="9e069-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="9e069-108">Каждый из трех компонентов (красный, зеленый, синий) данного исходного цвета смешивается с соответствующим компонентом цвета фона в соответствии со следующей формулой:</span><span class="sxs-lookup"><span data-stu-id="9e069-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="9e069-109">Дисплайколор = Саурцеколор × альфа/255 + backgroundColor x (255 – альфа)/255</span><span class="sxs-lookup"><span data-stu-id="9e069-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="9e069-110">Например, предположим, что красный компонент исходного цвета имеет значение 150, а красный компонент цвета фона — 100.</span><span class="sxs-lookup"><span data-stu-id="9e069-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="9e069-111">Если альфа-значение равно 200, то красный компонент результирующего цвета вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9e069-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="9e069-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="9e069-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="9e069-113">В следующих разделах более подробно рассматривается альфа-смешение:</span><span class="sxs-lookup"><span data-stu-id="9e069-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="9e069-114">Рисование непрозрачных и частично прозрачных линий</span><span class="sxs-lookup"><span data-stu-id="9e069-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="9e069-115">Рисование с помощью непрозрачных и полупрозрачных кистей</span><span class="sxs-lookup"><span data-stu-id="9e069-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="9e069-116">Использование режима компоновки для управления альфа-смешением</span><span class="sxs-lookup"><span data-stu-id="9e069-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="9e069-117">Использование матрицы цветов для настройки альфа-компонентов в изображениях</span><span class="sxs-lookup"><span data-stu-id="9e069-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="9e069-118">Установка альфа-значений отдельных пикселов</span><span class="sxs-lookup"><span data-stu-id="9e069-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



