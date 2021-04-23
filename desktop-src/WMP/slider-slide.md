---
title: ПОЛЗУНок. слайд
description: Атрибут «слайд» указывает или получает значение, указывающее, постепенно ли изображение переднего плана на фоне фонового изображения.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- ПОЛЗУНок. сдвинуть проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657721"
---
# <a name="sliderslide"></a><span data-ttu-id="b5ff4-104">ПОЛЗУНок. слайд</span><span class="sxs-lookup"><span data-stu-id="b5ff4-104">SLIDER.slide</span></span>

<span data-ttu-id="b5ff4-105">Атрибут « **слайд** » указывает или получает значение, указывающее, постепенно ли изображение переднего плана на фоне фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="b5ff4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b5ff4-106">Possible Values</span></span>

<span data-ttu-id="b5ff4-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b5ff4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ff4-108">Value</span></span> | <span data-ttu-id="b5ff4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b5ff4-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="b5ff4-110">true</span><span class="sxs-lookup"><span data-stu-id="b5ff4-110">true</span></span>  | <span data-ttu-id="b5ff4-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-111">Default.</span></span> <span data-ttu-id="b5ff4-112">Изображение переднего плана на фоне фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="b5ff4-113">false</span><span class="sxs-lookup"><span data-stu-id="b5ff4-113">false</span></span> | <span data-ttu-id="b5ff4-114">Изображение переднего плана раскрывается на месте фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5ff4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5ff4-115">Remarks</span></span>

<span data-ttu-id="b5ff4-116">При перемещении ползунка **сумбимаже** с помощью мыши, если параметру « **слайд** » присвоено значение true, то на слайдах с изображением переднего плана, как если бы он закрывать фоновое изображение, перемещается ползунок.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="b5ff4-117">Если параметру « **слайд** » присвоено значение false, то изображение переднего плана не перемещается, но выводится на месте, как если бы ползунок перемещает фоновое изображение за пределы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ff4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ff4-118">Requirements</span></span>



| <span data-ttu-id="b5ff4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ff4-119">Requirement</span></span> | <span data-ttu-id="b5ff4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ff4-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b5ff4-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b5ff4-121">Version</span></span><br/> | <span data-ttu-id="b5ff4-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b5ff4-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5ff4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5ff4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ff4-124">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="b5ff4-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="b5ff4-125">**ПОЛЗУНок. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="b5ff4-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="b5ff4-126">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="b5ff4-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





