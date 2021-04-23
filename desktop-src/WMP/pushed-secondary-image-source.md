---
title: Источник отправленного дополнительного образа
description: Источник отправленного дополнительного образа
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068049"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="b764e-108">Источник отправленного дополнительного образа</span><span class="sxs-lookup"><span data-stu-id="b764e-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="b764e-109">В зависимости от функции кнопки может потребоваться определить расположение отправленного изображения для дополнительного состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="b764e-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="b764e-110">Это будет изображение, которое пользователи видят при нажатии кнопки функции Плайпаусе во второй раз.</span><span class="sxs-lookup"><span data-stu-id="b764e-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="b764e-111">Чтобы определить этот образ, необходимо ввести тип изображения, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="b764e-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="b764e-112">Затем необходимо ввести два положительных целых числа, определяющие координаты левого верхнего угла (в пикселях) изображения, которое будет использоваться в типе изображения, из которого выполняется рисование.</span><span class="sxs-lookup"><span data-stu-id="b764e-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="b764e-113">Например, чтобы определить отправленное изображение для дополнительного источника изображения, если изображение находится внутри точечного рисунка, введите:</span><span class="sxs-lookup"><span data-stu-id="b764e-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="b764e-114">Дополнительные состояния не могут иметь отключенный образ.</span><span class="sxs-lookup"><span data-stu-id="b764e-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="b764e-115">Предполагается, что дополнительные образы имеют одинаковую ширину и высоту, чем основной образ.</span><span class="sxs-lookup"><span data-stu-id="b764e-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b764e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b764e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b764e-117">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="b764e-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




