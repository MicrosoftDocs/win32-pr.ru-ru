---
title: ПОЛЗУНок. Сумбимаже
description: Атрибут Сумбимаже указывает или получает изображение, которое будет использоваться для представления текущей положения ползунка.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- ПОЛЗУНок. Сумбимаже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698965"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="716f4-104">ПОЛЗУНок. Сумбимаже</span><span class="sxs-lookup"><span data-stu-id="716f4-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="716f4-105">Атрибут **сумбимаже** указывает или получает изображение, которое будет использоваться для представления текущей положения ползунка.</span><span class="sxs-lookup"><span data-stu-id="716f4-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="716f4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="716f4-106">Possible Values</span></span>

<span data-ttu-id="716f4-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="716f4-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="716f4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="716f4-108">Remarks</span></span>

<span data-ttu-id="716f4-109">**Сумбимаже** указывает изображение, которое будет использоваться для представления текущей позицией, а также указывает, что пользователь может выполнить действие с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="716f4-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="716f4-110">Если изображение Thumb не указано, ползунок не является интерактивным.</span><span class="sxs-lookup"><span data-stu-id="716f4-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="716f4-111">Изображение бегунка центрируется в узких измерениях элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="716f4-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="716f4-112">Если изображение Thumb является более узким, чем элемент управления, изображение отображается в центре фона.</span><span class="sxs-lookup"><span data-stu-id="716f4-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="716f4-113">Если изображение Thumb больше элемента управления, концы изображения будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="716f4-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="716f4-114">Положение ползунка задается центром изображения Thumb.</span><span class="sxs-lookup"><span data-stu-id="716f4-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="716f4-115">Если **бордерсизе** равен нулю, то на начальном и конечном ползунке будет отображаться только половина эскиза.</span><span class="sxs-lookup"><span data-stu-id="716f4-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="716f4-116">Чтобы предотвратить это, задайте для **бордерсизе** значение, которое больше или равно половине ширины изображения Thumb (или половины высоты, если для параметра **Direction** задано значение "вертикально").</span><span class="sxs-lookup"><span data-stu-id="716f4-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="716f4-117">Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="716f4-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="716f4-118">См. **кустомслидер**. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .</span><span class="sxs-lookup"><span data-stu-id="716f4-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="716f4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="716f4-119">Requirements</span></span>



| <span data-ttu-id="716f4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="716f4-120">Requirement</span></span> | <span data-ttu-id="716f4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="716f4-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="716f4-122">Версия</span><span class="sxs-lookup"><span data-stu-id="716f4-122">Version</span></span><br/> | <span data-ttu-id="716f4-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="716f4-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="716f4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="716f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716f4-125">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="716f4-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="716f4-126">**ПОЛЗУНок. Бордерсизе**</span><span class="sxs-lookup"><span data-stu-id="716f4-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="716f4-127">**ПОЛЗУНок. Direction**</span><span class="sxs-lookup"><span data-stu-id="716f4-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





