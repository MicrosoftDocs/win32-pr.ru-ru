---
title: ПОЛЗУНок. Фореграундимаже
description: Атрибут Фореграундимаже указывает или получает изображение переднего плана ползунка.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- ПОЛЗУНок. Фореграундимаже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657913"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="d4d02-104">ПОЛЗУНок. Фореграундимаже</span><span class="sxs-lookup"><span data-stu-id="d4d02-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="d4d02-105">Атрибут **фореграундимаже** указывает или получает изображение переднего плана ползунка.</span><span class="sxs-lookup"><span data-stu-id="d4d02-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="d4d02-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d4d02-106">Possible Values</span></span>

<span data-ttu-id="d4d02-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="d4d02-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d02-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4d02-108">Remarks</span></span>

<span data-ttu-id="d4d02-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4d02-109">This attribute is optional.</span></span> <span data-ttu-id="d4d02-110">При использовании изображений для создания элемента управления "ползунок" **фоновый** рисунок используется для основного изображения ползунка.</span><span class="sxs-lookup"><span data-stu-id="d4d02-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="d4d02-111">**Сумбимаже** представляет фактический ползунок и может быть перемещен с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="d4d02-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="d4d02-112">На ползунке **сумбимаже** отображается невидимая строка, в которой фоновое изображение отображается на одной стороне линии, а изображение переднего плана отображается на другой стороне.</span><span class="sxs-lookup"><span data-stu-id="d4d02-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="d4d02-113">При перемещении ползунка **сумбимаже** с помощью мыши, если параметру « **слайд** » присвоено значение true, то на слайдах с изображением переднего плана, как если бы он закрывать фоновое изображение, перемещается ползунок.</span><span class="sxs-lookup"><span data-stu-id="d4d02-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="d4d02-114">Если параметру « **слайд** » присвоено значение false, то изображение переднего плана не перемещается, но выводится на месте, как если бы ползунок перемещает фоновое изображение за пределы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="d4d02-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="d4d02-115">Если для атрибута **мозаичного заполнения** задано значение true, а изображение переднего плана меньше, чем область переднего плана, изображение будет мозаично заполнено горизонтально или вертикально, в зависимости от атрибута **Direction** , чтобы заполнить доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="d4d02-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="d4d02-116">Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="d4d02-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d02-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d02-117">Requirements</span></span>



| <span data-ttu-id="d4d02-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d02-118">Requirement</span></span> | <span data-ttu-id="d4d02-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d02-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d4d02-120">Версия</span><span class="sxs-lookup"><span data-stu-id="d4d02-120">Version</span></span><br/> | <span data-ttu-id="d4d02-121">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d4d02-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4d02-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d02-123">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="d4d02-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="d4d02-124">**ПОЛЗУНок. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="d4d02-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="d4d02-125">**ПОЛЗУНок. слайд**</span><span class="sxs-lookup"><span data-stu-id="d4d02-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="d4d02-126">**ПОЛЗУНок. Сумбимаже**</span><span class="sxs-lookup"><span data-stu-id="d4d02-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="d4d02-127">**ПОЛЗУНок. Value**</span><span class="sxs-lookup"><span data-stu-id="d4d02-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





