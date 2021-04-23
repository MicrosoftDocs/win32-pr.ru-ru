---
description: 'Возможны ситуации, когда необходимо создать экран, который имеет следующие характеристики:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Использование режима компоновки для управления альфа-смешением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985116"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="b9c6d-103">Использование режима компоновки для управления альфа-смешением</span><span class="sxs-lookup"><span data-stu-id="b9c6d-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="b9c6d-104">Возможны ситуации, когда необходимо создать экран, который имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="b9c6d-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="b9c6d-105">Цвета имеют альфа-значения менее 255.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="b9c6d-106">Цвета не смешиваются с альфа-смешением при создании точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="b9c6d-107">При отображении готового точечного рисунка цвета в точечном рисунке смешиваются с цветами фона на устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="b9c6d-108">Чтобы создать такой точечный рисунок, создайте пустой [**растровый**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объект, а затем создайте [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе этого растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="b9c6d-109">Установите режим компоновки объекта **Graphics** равным компоситингмодесаурцекопи.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="b9c6d-110">В следующем примере создается [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе объекта [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="b9c6d-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="b9c6d-111">Код использует объект **Graphics** вместе с двумя полупрозрачными кистями (альфа = 160) для рисования на точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="b9c6d-112">Код заполняет красный эллипс и зеленый эллипс с помощью полупрозрачных кистей.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="b9c6d-113">Зеленый эллипс пересекается с красным эллипсом, но зеленый не смешивается с красным, так как режим композиции объекта **Graphics** имеет значение компоситингмодесаурцекопи.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="b9c6d-114">Далее код готовится к рисованию на экране путем вызова [бегинпаинт](/windows/win32/api/winuser/nf-winuser-beginpaint) и создания [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на основе контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="b9c6d-115">Код рисует растровое изображение на экране дважды: один раз на белом фоне и один раз в многоцветном фоне.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="b9c6d-116">Пиксели точечного рисунка, являющиеся частью двух эллипсов, имеют альфа-компонент 160, поэтому эллипсы смешиваются с фоновыми цветами на экране.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="b9c6d-117">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="b9c6d-118">Обратите внимание, что эллипсы смешиваются с фоном, но они не смешиваются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![Иллюстрация, демонстрирующая два различных цветных эллипса, каждый из которых смешивается с многоцветным фоном](images/sourcecopy.png)

<span data-ttu-id="b9c6d-120">В предыдущем примере кода содержится следующая инструкция:</span><span class="sxs-lookup"><span data-stu-id="b9c6d-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="b9c6d-121">Если нужно смешивать эллипсы друг с другом, а также с фоном, измените эту инструкцию следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b9c6d-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="b9c6d-122">На следующем рисунке показаны выходные данные измененного кода.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-122">The following illustration shows the output of the revised code.</span></span>

![Использование режима компоновки для управления иллюстрацией альфа-смешения](images/sourceover.png)

 

 



