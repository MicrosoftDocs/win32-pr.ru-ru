---
description: Если в метод DrawImage передается только левый верхний угол изображения, Windows GDI+ может масштабировать изображение, что приведет к снижению производительности.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Повышение производительности за счет предотвращения автоматического масштабирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985164"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="9f5bc-103">Повышение производительности за счет предотвращения автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="9f5bc-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="9f5bc-104">Если в метод **DrawImage** передается только левый верхний угол изображения, Windows GDI+ может масштабировать изображение, что приведет к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="9f5bc-105">Следующий вызов метода **DrawImage** задает левый верхний угол (50, 30), но не задает прямоугольник назначения:</span><span class="sxs-lookup"><span data-stu-id="9f5bc-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="9f5bc-106">Хотя это самая простая версия метода **DrawImage** с точки зрения количества обязательных аргументов, она не обязательно является самой эффективной.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="9f5bc-107">Если количество точек на дюйм на текущем устройстве отображения отличается от количества точек на дюйм на устройстве, где был создан образ, GDI+ масштабирует изображение таким образом, чтобы его физический размер на текущем устройстве отображался максимально близко к физическому размеру на устройстве, где оно было создано.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="9f5bc-108">Если вы хотите предотвратить такое масштабирование, передайте ширину и высоту прямоугольника назначения методу **DrawImage** .</span><span class="sxs-lookup"><span data-stu-id="9f5bc-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="9f5bc-109">В следующем примере одно и то же изображение рисуется дважды.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-109">The following example draws the same image twice.</span></span> <span data-ttu-id="9f5bc-110">В первом случае ширина и высота прямоугольника назначения не указываются, а изображение автоматически масштабируется.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="9f5bc-111">Во втором случае ширина и высота (измеряемая в пикселях) прямоугольника назначения указываются так же, как ширина и высота исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="9f5bc-112">На следующем рисунке показано изображение, отображаемое дважды.</span><span class="sxs-lookup"><span data-stu-id="9f5bc-112">The following illustration shows the image rendered twice.</span></span>

![снимок экрана окна, содержащего две версии одного изображения с разными шкалами](images/scaledtexture1.png)

 

 



