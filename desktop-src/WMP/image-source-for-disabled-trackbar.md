---
title: Источник изображения для отключенной TrackBar
description: Источник изображения для отключенной TrackBar
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, линейки воспроизведения
- обложки, TrackBar
- Справочник по обложек, TrackBar
- линейки воспроизведения в обложках, источник изображения
- Источник изображения для обложек, TrackBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691226"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="3ab86-108">Источник изображения для отключенной TrackBar</span><span class="sxs-lookup"><span data-stu-id="3ab86-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="3ab86-109">Необходимо определить источник изображения, которое должно отображаться при отключении TrackBar, используя тип точечного рисунка, из которого нужно создать изображение.</span><span class="sxs-lookup"><span data-stu-id="3ab86-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="3ab86-110">Отображаемый образ обычно находится внутри файла Super или при создании обложки для проигрывателя Windows Media 10 Mobile этот образ будет находиться в файле Сиксумб.</span><span class="sxs-lookup"><span data-stu-id="3ab86-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="3ab86-111">Необходимо ввести тип образа, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="3ab86-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="3ab86-112">Затем необходимо ввести два положительных целых числа, определяющие координаты верхнего левого угла (в пикселях) изображения, которое нужно использовать внутри типа точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="3ab86-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="3ab86-113">Например, чтобы использовать изображение из точечного рисунка Сиксумб с верхним и левым положением 50, 60 пикселей, введите:</span><span class="sxs-lookup"><span data-stu-id="3ab86-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="3ab86-114">Необходимо определить расположение изображения для отключенного изображения TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3ab86-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="3ab86-115">Если вы не хотите отображать новый образ, можно определить фоновое изображение в качестве отключенного изображения со смещением 0, 0:</span><span class="sxs-lookup"><span data-stu-id="3ab86-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="3ab86-116">В предыдущем примере 50, 60 означает расположение кнопки, с которой вы работаете, в файле Сиксумб (в данном случае это то же расположение, что и кнопка на фоновом рисунке).</span><span class="sxs-lookup"><span data-stu-id="3ab86-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="3ab86-117">Однако настоятельно рекомендуется отображать отключенный образ для всех значений TrackBar, чтобы дать пользователю визуальную индикацию, поскольку ползунки не будут работать при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="3ab86-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="3ab86-118">Например, если текущий список воспроизведения пуст, могут быть отключены линейки по поиску.</span><span class="sxs-lookup"><span data-stu-id="3ab86-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ab86-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3ab86-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab86-120">**Линейки воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="3ab86-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




