---
title: Линейки воспроизведения
description: Линейки воспроизведения
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, линейки воспроизведения
- обложки, TrackBar
- Справочник по обложек, TrackBar
- Ползунки в обложках, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700649"
---
# <a name="trackbars"></a><span data-ttu-id="0938d-107">Линейки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="0938d-107">Trackbars</span></span>

<span data-ttu-id="0938d-108">Значение TrackBar отображает изображение, которое изменяется мелкими приращениями.</span><span class="sxs-lookup"><span data-stu-id="0938d-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="0938d-109">Ползунки используются для элементов управления "Громкость" и "расположение воспроизведения".</span><span class="sxs-lookup"><span data-stu-id="0938d-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="0938d-110">Ползунки можно использовать для вывода сведений о текущем элементе мультимедиа или для разрешения пользователю изменять параметры или позицию воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0938d-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="0938d-111">Например, можно использовать параметр TrackBar, чтобы разрешить пользователю настраивать том, и другую линейку, которая может показывать пользователю текущую точку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0938d-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="0938d-112">Ползунки имеют изображение Thumb, определяющее текущее значение параметра TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0938d-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="0938d-113">Раздел TrackBar в файле определения обложки должен начинаться с этой строки:</span><span class="sxs-lookup"><span data-stu-id="0938d-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="0938d-114">Затем необходимо добавить одну или несколько строк, содержащих сведения о каждой из значений TrackBar в обложке.</span><span class="sxs-lookup"><span data-stu-id="0938d-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="0938d-115">Для раздела TrackBar файла определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="0938d-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="0938d-116">Чтобы получить сведения о TrackBar для каждой строки в разделе TrackBar (требуется каждая часть строки), необходимо использовать следующий порядок:</span><span class="sxs-lookup"><span data-stu-id="0938d-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="0938d-117">Тип TrackBar</span><span class="sxs-lookup"><span data-stu-id="0938d-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="0938d-118">Расположение TrackBar</span><span class="sxs-lookup"><span data-stu-id="0938d-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="0938d-119">Источник изображения для отключенной TrackBar</span><span class="sxs-lookup"><span data-stu-id="0938d-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="0938d-120">Источник изображения Thumb</span><span class="sxs-lookup"><span data-stu-id="0938d-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="0938d-121">Размер бегунка</span><span class="sxs-lookup"><span data-stu-id="0938d-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="0938d-122">Пример кода для TrackBar см. в [разделе Sample TrackBar](sample-trackbars-section.md).</span><span class="sxs-lookup"><span data-stu-id="0938d-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0938d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0938d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0938d-124">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="0938d-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




