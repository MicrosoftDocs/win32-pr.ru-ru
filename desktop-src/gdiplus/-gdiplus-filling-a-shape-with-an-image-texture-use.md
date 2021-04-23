---
description: Замкнутую фигуру можно заполнить текстурой с помощью класса Image и класса TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Заполнение фигуры текстурой изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156187"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="5e17e-103">Заполнение фигуры текстурой изображения</span><span class="sxs-lookup"><span data-stu-id="5e17e-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="5e17e-104">Замкнутую фигуру можно заполнить текстурой с помощью класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и класса [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="5e17e-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="5e17e-105">В следующем примере заливка эллипса осуществляется с помощью изображения.</span><span class="sxs-lookup"><span data-stu-id="5e17e-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="5e17e-106">Код конструирует объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , а затем передает адрес этого объекта **Image** в качестве аргумента в конструктор [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="5e17e-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="5e17e-107">Третья инструкция Code масштабирует изображение, а четвертый оператор заполняет эллипс повторяющимися копиями масштабированного изображения:</span><span class="sxs-lookup"><span data-stu-id="5e17e-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="5e17e-108">В предыдущем примере кода метод [**TextureBrush:: сеттрансформ**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) задает преобразование, которое применяется к изображению перед его прорисовкой.</span><span class="sxs-lookup"><span data-stu-id="5e17e-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="5e17e-109">Предположим, что исходное изображение имеет ширину 640 пикселей и высоту 480 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5e17e-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="5e17e-110">Преобразование сжимает изображение до 75 × 75, устанавливая горизонтальные и вертикальные значения масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5e17e-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="5e17e-111">В предыдущем примере размер изображения составляет 75 × 75, а размер эллипса — 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="5e17e-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="5e17e-112">Поскольку изображение меньше, чем заливка, эллипс заполняется изображением.</span><span class="sxs-lookup"><span data-stu-id="5e17e-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="5e17e-113">Мозаичное заполнение означает, что изображение повторяется горизонтально и вертикально до тех пор, пока не будет достигнута граница фигуры.</span><span class="sxs-lookup"><span data-stu-id="5e17e-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="5e17e-114">Дополнительные сведения о мозаичном заполнении см. в разделе [Мозаичное заполнение фигуры изображением](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="5e17e-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



