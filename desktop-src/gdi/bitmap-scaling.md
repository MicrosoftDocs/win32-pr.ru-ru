---
description: Функция Стретчблт масштабирует точечный рисунок, выполняя перенаправление битового блока из прямоугольника в исходном контексте устройства в прямоугольник в контексте целевого устройства.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Масштабирование растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155694"
---
# <a name="bitmap-scaling"></a><span data-ttu-id="b57cd-103">Масштабирование растрового изображения</span><span class="sxs-lookup"><span data-stu-id="b57cd-103">Bitmap Scaling</span></span>

<span data-ttu-id="b57cd-104">Функция [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) масштабирует точечный рисунок, выполняя перенаправление битового блока из прямоугольника в исходном контексте устройства в прямоугольник в контексте целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="b57cd-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="b57cd-105">Однако в отличие от функции [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , которая дублирует размеры исходного прямоугольника в прямоугольнике назначения, **стретчблт** позволяет приложению указывать размеры исходных и целевых прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="b57cd-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="b57cd-106">Если точечный рисунок назначения меньше исходного точечного рисунка, система объединяет строки или столбцы цветовых данных (или и то, и другое) в точечный рисунок перед отрисовкой соответствующего изображения на устройстве отображения.</span><span class="sxs-lookup"><span data-stu-id="b57cd-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="b57cd-107">Система объединяет данные цвета в соответствии с заданным режимом растяжения, который определяется приложением путем вызова функции [**сетстретчблтмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) .</span><span class="sxs-lookup"><span data-stu-id="b57cd-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="b57cd-108">Если размер битовой карты назначения больше, чем исходный точечный рисунок, система масштабирует или увеличивает каждый пиксель в результирующем изображении соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b57cd-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



