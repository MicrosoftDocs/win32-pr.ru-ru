---
title: Нормальный источник третьего образа
description: Нормальный источник третьего образа
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411243"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="9ccb6-108">Нормальный источник третьего образа</span><span class="sxs-lookup"><span data-stu-id="9ccb6-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="9ccb6-109">Функция кнопки Плайпаусестоп требует, чтобы вы определили расположение обычного изображения для третьего состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="9ccb6-110">Это будет изображение, которое пользователи видят после нажатия кнопки Плайпаусестоп, чтобы начать потоковую передачу вещания в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="9ccb6-111">Чтобы определить этот образ, необходимо ввести тип изображения, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="9ccb6-112">Затем необходимо ввести два положительных целых числа, определяющие координаты верхнего левого угла (в пикселях) изображения, которое нужно использовать внутри типа точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="9ccb6-113">Например, чтобы определить нормальный образ для источника "третичное изображение", если изображение находится внутри точечного рисунка, введите:</span><span class="sxs-lookup"><span data-stu-id="9ccb6-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="9ccb6-114">В третичных состояниях не может быть отключенного образа.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="9ccb6-115">Предполагается, что для третьего и дополнительного образов используются одинаковые значения ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ccb6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9ccb6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccb6-117">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="9ccb6-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




