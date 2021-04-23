---
title: Нормальный источник вторичного образа
description: Нормальный источник вторичного образа
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691339"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="42da0-108">Нормальный источник вторичного образа</span><span class="sxs-lookup"><span data-stu-id="42da0-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="42da0-109">В зависимости от функции кнопки может потребоваться определить расположение обычного изображения для дополнительного состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="42da0-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="42da0-110">Это будет изображение, которое пользователи видят при первой нажатии кнопки функции Плайпаусе.</span><span class="sxs-lookup"><span data-stu-id="42da0-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="42da0-111">Чтобы определить этот образ, необходимо ввести тип изображения, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="42da0-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="42da0-112">Затем необходимо ввести два положительных целых числа, определяющие координаты верхнего левого угла (в пикселях) изображения, которое нужно использовать внутри типа точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="42da0-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="42da0-113">Например, чтобы определить нормальный образ для вторичного источника изображения, если изображение находится внутри помещенного точечного рисунка, введите:</span><span class="sxs-lookup"><span data-stu-id="42da0-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="42da0-114">Дополнительные состояния не могут иметь отключенный образ.</span><span class="sxs-lookup"><span data-stu-id="42da0-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="42da0-115">Предполагается, что дополнительные образы имеют одинаковую ширину и высоту, чем основной образ.</span><span class="sxs-lookup"><span data-stu-id="42da0-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42da0-116">См. также</span><span class="sxs-lookup"><span data-stu-id="42da0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42da0-117">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="42da0-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




