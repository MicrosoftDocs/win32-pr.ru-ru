---
title: ПОЛЗУНок. мозаичный
description: Атрибут мозаичного заполнения указывает или получает значение, указывающее, будет ли мозаичное изображение перемещено.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- ПОЛЗУНок. мозаичный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657337"
---
# <a name="slidertiled"></a><span data-ttu-id="61fa1-104">ПОЛЗУНок. мозаичный</span><span class="sxs-lookup"><span data-stu-id="61fa1-104">SLIDER.tiled</span></span>

<span data-ttu-id="61fa1-105">Атрибут **мозаичного заполнения** указывает или получает значение, указывающее, будет ли мозаичное изображение перемещено.</span><span class="sxs-lookup"><span data-stu-id="61fa1-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="61fa1-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="61fa1-106">Possible Values</span></span>

<span data-ttu-id="61fa1-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="61fa1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="61fa1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="61fa1-108">Value</span></span> | <span data-ttu-id="61fa1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="61fa1-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fa1-110">true</span><span class="sxs-lookup"><span data-stu-id="61fa1-110">true</span></span>  | <span data-ttu-id="61fa1-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61fa1-111">Default.</span></span> <span data-ttu-id="61fa1-112">Точечный рисунок изображения повторяется до тех пор, пока не будет заполнен весь регион элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61fa1-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="61fa1-113">false</span><span class="sxs-lookup"><span data-stu-id="61fa1-113">false</span></span> | <span data-ttu-id="61fa1-114">Изображение не будет мозаичным.</span><span class="sxs-lookup"><span data-stu-id="61fa1-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="61fa1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61fa1-115">Remarks</span></span>

<span data-ttu-id="61fa1-116">Этот атрибут применяется только в том случае, если для определения элемента управления используется цвет переднего плана и фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="61fa1-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="61fa1-117">Если изображения меньше, чем определенная область ползунка, а атрибут **мозаичного заполнения** имеет значение true, изображения будут повторяться до тех пор, пока не будут заполнены все элементы управления.</span><span class="sxs-lookup"><span data-stu-id="61fa1-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="61fa1-118">Этот атрибут можно использовать вместе с атрибутом **бордерсизе** .</span><span class="sxs-lookup"><span data-stu-id="61fa1-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="61fa1-119">Атрибут **бордерсизе** позволяет определить границу, которая не повторяется во время мозаичного заполнения.</span><span class="sxs-lookup"><span data-stu-id="61fa1-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="61fa1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="61fa1-120">Requirements</span></span>



| <span data-ttu-id="61fa1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="61fa1-121">Requirement</span></span> | <span data-ttu-id="61fa1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="61fa1-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="61fa1-123">Версия</span><span class="sxs-lookup"><span data-stu-id="61fa1-123">Version</span></span><br/> | <span data-ttu-id="61fa1-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="61fa1-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61fa1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61fa1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fa1-126">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="61fa1-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="61fa1-127">**ПОЛЗУНок. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="61fa1-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="61fa1-128">**ПОЛЗУНок. Бордерсизе**</span><span class="sxs-lookup"><span data-stu-id="61fa1-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="61fa1-129">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="61fa1-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





