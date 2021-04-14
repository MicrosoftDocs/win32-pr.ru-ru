---
description: Вместо того, чтобы рисовать линию или кривую сплошным цветом, можно рисовать текстурой.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Рисование линии, заполненной текстурой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985185"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="e24a0-103">Рисование линии, заполненной текстурой</span><span class="sxs-lookup"><span data-stu-id="e24a0-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="e24a0-104">Вместо того, чтобы рисовать линию или кривую сплошным цветом, можно рисовать текстурой.</span><span class="sxs-lookup"><span data-stu-id="e24a0-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="e24a0-105">Чтобы нарисовать линии и кривые с текстурой, создайте объект [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) и передайте адрес этого объекта **TextureBrush** конструктору [**пера**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e24a0-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="e24a0-106">Изображение, связанное с текстурной кистью, используется для мозаичного заполнения плоскости (незаметно), а когда перо рисует линию или кривую, штрих пера обнаруживает определенные Пиксели мозаичной текстуры.</span><span class="sxs-lookup"><span data-stu-id="e24a0-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="e24a0-107">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Texture1.jpg.</span><span class="sxs-lookup"><span data-stu-id="e24a0-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="e24a0-108">Этот образ используется для создания объекта [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , а объект **TextureBrush** используется для создания объекта [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e24a0-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e24a0-109">Вызов [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) рисует изображение с его верхним левым углом в точке (0, 0).</span><span class="sxs-lookup"><span data-stu-id="e24a0-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="e24a0-110">Вызов [**Graphics::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) использует объект **Pen** для рисования текстурированного эллипса.</span><span class="sxs-lookup"><span data-stu-id="e24a0-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="e24a0-111">На следующем рисунке показано изображение и текстурированный эллипс.</span><span class="sxs-lookup"><span data-stu-id="e24a0-111">The following illustration shows the image and the textured ellipse.</span></span>

![Иллюстрация, показывающая небольшое прямоугольное изображение, а сегмент эллиптической линии заполняется исходным изображением](images/pens7.png)

 

 
