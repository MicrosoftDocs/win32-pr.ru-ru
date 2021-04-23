---
title: ПОЛЗУНок. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение ползунка.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- SLIDER. backgroundImage проигрывателя Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656940"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="30669-104">ПОЛЗУНок. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="30669-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="30669-105">Атрибут **backgroundImage** указывает или получает фоновое изображение ползунка.</span><span class="sxs-lookup"><span data-stu-id="30669-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="30669-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="30669-106">Possible Values</span></span>

<span data-ttu-id="30669-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="30669-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="30669-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30669-108">Remarks</span></span>

<span data-ttu-id="30669-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30669-109">This attribute is optional.</span></span> <span data-ttu-id="30669-110">При использовании изображений для создания ползунка используется **фоновый** рисунок для основного изображения ползунка.</span><span class="sxs-lookup"><span data-stu-id="30669-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="30669-111">**Сумбимаже** представляет фактический ползунок и может быть перемещен с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="30669-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="30669-112">На ползунке **сумбимаже** отображается невидимая строка, в которой фоновое изображение отображается на одной стороне линии, а изображение переднего плана отображается на другой стороне.</span><span class="sxs-lookup"><span data-stu-id="30669-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="30669-113">При перемещении ползунка **сумбимаже** с помощью мыши, если параметру « **слайд** » присвоено значение true, то на слайдах с изображением переднего плана, как если бы он закрывать фоновое изображение, перемещается ползунок.</span><span class="sxs-lookup"><span data-stu-id="30669-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="30669-114">Если параметру « **слайд** » присвоено значение false, то изображение переднего плана не перемещается, но выводится на месте, как если бы ползунок перемещает фоновое изображение за пределы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="30669-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="30669-115">Если атрибут **мозаичного заполнения** имеет значение true, а фоновое изображение меньше, чем элемент управления Slider, изображение будет мозаично перемещаться по горизонтали или по вертикали в зависимости от атрибута **Direction** .</span><span class="sxs-lookup"><span data-stu-id="30669-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="30669-116">Если для атрибута **бордерсизе** задано значение больше нуля, указанное число будет равно числу пикселей слева, справа или сверху и снизу изображения (опять, в зависимости от атрибута **направления** ), который будет зарезервирован для границ элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="30669-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="30669-117">В этом случае для разбиения оставшейся части элемента управления используется только Центральная часть изображения.</span><span class="sxs-lookup"><span data-stu-id="30669-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="30669-118">Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="30669-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="30669-119">Требования</span><span class="sxs-lookup"><span data-stu-id="30669-119">Requirements</span></span>



| <span data-ttu-id="30669-120">Требование</span><span class="sxs-lookup"><span data-stu-id="30669-120">Requirement</span></span> | <span data-ttu-id="30669-121">Значение</span><span class="sxs-lookup"><span data-stu-id="30669-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="30669-122">Версия</span><span class="sxs-lookup"><span data-stu-id="30669-122">Version</span></span><br/> | <span data-ttu-id="30669-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="30669-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30669-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30669-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30669-125">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="30669-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="30669-126">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="30669-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="30669-127">**ПОЛЗУНок. слайд**</span><span class="sxs-lookup"><span data-stu-id="30669-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="30669-128">**ПОЛЗУНок. Сумбимаже**</span><span class="sxs-lookup"><span data-stu-id="30669-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





