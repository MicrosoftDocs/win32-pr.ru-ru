---
description: Можно поворачивать, отражать и расклонять изображение, указывая конечные точки для верхнего левого, верхнего правого и нижнего левого углов исходного изображения.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Вращение, отражение и наклон изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991633"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="37f79-103">Вращение, отражение и наклон изображений</span><span class="sxs-lookup"><span data-stu-id="37f79-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="37f79-104">Можно поворачивать, отражать и расклонять изображение, указывая конечные точки для верхнего левого, верхнего правого и нижнего левого углов исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="37f79-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="37f79-105">Три точки назначения определяют аффинное преобразование, которое сопоставляет исходное прямоугольное изображение с параллелограмм.</span><span class="sxs-lookup"><span data-stu-id="37f79-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="37f79-106">(Правый нижний угол исходного изображения сопоставляется с четвертым углом параллелограмма, который вычисляется по трем указанным конечным точкам.)</span><span class="sxs-lookup"><span data-stu-id="37f79-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="37f79-107">Например, предположим, что исходный рисунок представляет собой прямоугольник с верхним левым углом в (0, 0), правый верхний угол в (100, 0), а нижний левый угол в (0, 50).</span><span class="sxs-lookup"><span data-stu-id="37f79-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="37f79-108">Теперь предположим, что эти три точки сопоставляются с конечными точками следующим образом.</span><span class="sxs-lookup"><span data-stu-id="37f79-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="37f79-109">Исходная точка</span><span class="sxs-lookup"><span data-stu-id="37f79-109">Original point</span></span>       | <span data-ttu-id="37f79-110">Конечная точка</span><span class="sxs-lookup"><span data-stu-id="37f79-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="37f79-111">Верхний левый (0, 0)</span><span class="sxs-lookup"><span data-stu-id="37f79-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="37f79-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="37f79-112">(200, 20)</span></span>         |
| <span data-ttu-id="37f79-113">Верхний правый (100, 0)</span><span class="sxs-lookup"><span data-stu-id="37f79-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="37f79-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="37f79-114">(110, 100)</span></span>        |
| <span data-ttu-id="37f79-115">Нижний левый (0, 50)</span><span class="sxs-lookup"><span data-stu-id="37f79-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="37f79-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="37f79-116">(250, 30)</span></span>         |



 

<span data-ttu-id="37f79-117">На следующем рисунке показано исходное изображение и изображение, сопоставленное с параллелограмм.</span><span class="sxs-lookup"><span data-stu-id="37f79-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="37f79-118">Исходное изображение было наклонено, отражено, повернуто и переведено.</span><span class="sxs-lookup"><span data-stu-id="37f79-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="37f79-119">Ось x на верхнем крае исходного изображения сопоставляется со строкой, которая выполняется через (200, 20) и (110, 100).</span><span class="sxs-lookup"><span data-stu-id="37f79-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="37f79-120">Ось y на левом крае исходного изображения сопоставляется со строкой, которая выполняется через (200, 20) и (250, 30).</span><span class="sxs-lookup"><span data-stu-id="37f79-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![Иллюстрация, показывающая цветные полосы в источнике осей координат, и одни и те же полосы наклонены и в другом расположении, повороте и размере](images/stripes1.png)

<span data-ttu-id="37f79-122">В следующем примере создаются изображения, показанные на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="37f79-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="37f79-123">На следующем рисунке показано аналогичное преобразование, применяемое к фотографному изображению.</span><span class="sxs-lookup"><span data-stu-id="37f79-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![Иллюстрация, показывающая одну и ту же фотографию дважды; второй — обратный, наклоненный и имеет другой размер, поворот и расположение.](images/transformedclimber.png)

<span data-ttu-id="37f79-125">На следующем рисунке показано аналогичное преобразование, применяемое к метафайлу.</span><span class="sxs-lookup"><span data-stu-id="37f79-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![Иллюстрация, отображающая фигуры и текст, а также обратную, наклоненную и с разными расположением, поворотом и размером.](images/transformedmetafile.png)

 

 



