---
title: Источник отправленного третьего образа
description: Источник отправленного третьего образа
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986501"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="7b9a7-108">Источник отправленного третьего образа</span><span class="sxs-lookup"><span data-stu-id="7b9a7-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="7b9a7-109">Функция кнопки Плайпаусестоп требует, чтобы вы определили расположение отправленного изображения для третьего состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="7b9a7-110">Это будет изображение, которое пользователи видят при нажатии кнопки Плайпаусестоп при потоковой передаче широковещательной передачи в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="7b9a7-111">Чтобы определить этот образ, необходимо ввести тип изображения, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="7b9a7-112">Затем необходимо ввести два положительных целых числа, определяющие координаты верхнего левого угла (в пикселях) изображения, которое нужно использовать внутри типа точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="7b9a7-113">Например, чтобы определить отправленный образ для источника третьего образа, если изображение находится внутри точечного рисунка, введите:</span><span class="sxs-lookup"><span data-stu-id="7b9a7-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="7b9a7-114">В третичных состояниях не может быть отключенного образа.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="7b9a7-115">Предполагается, что для третьего и дополнительного образов используются одинаковые значения ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b9a7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7b9a7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b9a7-117">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="7b9a7-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




