---
title: Источник отправленного изображения
description: Источник отправленного изображения
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777090"
---
# <a name="pushed-image-source"></a><span data-ttu-id="b00c3-108">Источник отправленного изображения</span><span class="sxs-lookup"><span data-stu-id="b00c3-108">Pushed Image Source</span></span>

<span data-ttu-id="b00c3-109">Необходимо определить источник изображения, которое должно отображаться при принудительной отправке пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="b00c3-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="b00c3-110">Образ берется из файла, который вы определили как отправленный в разделе "точечные рисунки".</span><span class="sxs-lookup"><span data-stu-id="b00c3-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="b00c3-111">Необходимо ввести тип образа, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="b00c3-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="b00c3-112">Затем необходимо ввести два положительных целых числа, определяющие верхнюю и левую координаты (в пикселях) изображения, которое нужно использовать внутри файла изображения.</span><span class="sxs-lookup"><span data-stu-id="b00c3-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="b00c3-113">Расположение, в котором будет отображаться изображение, берется из координат, определенных для кнопки относительно фонового изображения; но расположение, из которого оно берется, определяется двумя числами, указанными в параметре @, и отсчитывается от отправленного изображения, из которого считывается изображение.</span><span class="sxs-lookup"><span data-stu-id="b00c3-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="b00c3-114">Например, чтобы использовать изображение из отправленного изображения, нарасположенного в отправленном файле, левый верхний край которого равен 50, 60 следует использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="b00c3-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="b00c3-115">Если вы не хотите отображать другое изображение, можно определить фоновый рисунок в качестве растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b00c3-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="b00c3-116">Для этого укажите фоновый файл в качестве отправленного файла и укажите смещение в левом верхнем углу кнопки:</span><span class="sxs-lookup"><span data-stu-id="b00c3-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="b00c3-117">В этом случае ни одна из кнопок не сможет отобразить отправленное изображение.</span><span class="sxs-lookup"><span data-stu-id="b00c3-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="b00c3-118">Рекомендуется отображать отправленное изображение для всех кнопок, чтобы дать пользователю наглядное представление, так как не всегда ясно, дает ли касание результат, особенно при воспроизведении музыки или при отключении звука касания.</span><span class="sxs-lookup"><span data-stu-id="b00c3-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b00c3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b00c3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b00c3-120">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="b00c3-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




