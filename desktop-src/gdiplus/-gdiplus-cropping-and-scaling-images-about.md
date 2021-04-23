---
title: Сведения об обрезке и масштабировании изображений GDI+
description: Для рисования и позиционирования изображений можно использовать метод DrawImage класса Graphics.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156199"
---
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="787fe-103">Сведения об обрезке и масштабировании изображений GDI+</span><span class="sxs-lookup"><span data-stu-id="787fe-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="787fe-104">Для рисования и позиционирования изображений можно использовать метод [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="787fe-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="787fe-105">Метод DrawImage является перегруженным методом, поэтому его можно указать несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="787fe-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="787fe-106">Один из вариаций метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) получает адрес объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) и ссылку на объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) .</span><span class="sxs-lookup"><span data-stu-id="787fe-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="787fe-107">Прямоугольник задает назначение для операции рисования. то есть он указывает прямоугольник, в котором будет нарисован изображение.</span><span class="sxs-lookup"><span data-stu-id="787fe-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="787fe-108">Если размер конечного прямоугольника отличается от размера исходного изображения, изображение масштабируется в соответствии с конечным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="787fe-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="787fe-109">В следующем примере один и тот же образ рисуется три раза: один раз без масштабирования, один раз с расширением и один раз с сжатием.</span><span class="sxs-lookup"><span data-stu-id="787fe-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="787fe-110">Приведенный выше код, а также определенный файл Spiral.png, выдают следующие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="787fe-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![Иллюстрация, отображающая три версии изображения: обычная, растянута в ширину и сжата до половины исходного размера](images/aboutgdip03-art06.png)

<span data-ttu-id="787fe-112">Некоторые разновидности метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) имеют параметр исходного прямоугольника, а также параметр конечного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="787fe-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="787fe-113">Исходный прямоугольник определяет часть исходного изображения, которая будет изображена.</span><span class="sxs-lookup"><span data-stu-id="787fe-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="787fe-114">Прямоугольник назначения определяет, где будет отображаться эта часть изображения.</span><span class="sxs-lookup"><span data-stu-id="787fe-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="787fe-115">Если размер конечного прямоугольника отличается от размера исходного прямоугольника, изображение масштабируется в соответствии с конечным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="787fe-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="787fe-116">В следующем примере объект [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) создается из файла Runner.jpg.</span><span class="sxs-lookup"><span data-stu-id="787fe-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="787fe-117">Изображение целиком рисуется без масштабирования в (0, 0).</span><span class="sxs-lookup"><span data-stu-id="787fe-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="787fe-118">Затем небольшая часть изображения рисуется дважды: один раз с сжатием и один раз с расширением.</span><span class="sxs-lookup"><span data-stu-id="787fe-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



<span data-ttu-id="787fe-119">На следующем рисунке показано немасштабированное изображение, а также сжатые и развернутые фрагменты изображений.</span><span class="sxs-lookup"><span data-stu-id="787fe-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![снимок экрана с изображением, затем частью сжатого изображения и той же развернутой частью](images/aboutgdip03-art07.png)

 

 



