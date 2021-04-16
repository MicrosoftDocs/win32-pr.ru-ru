---
title: ПОЛЗУНок. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона элемента управления "ползунок".
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- ПОЛЗУНок. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656942"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="b676a-104">ПОЛЗУНок. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b676a-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="b676a-105">Атрибут **backgroundColor** указывает или получает цвет фона элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="b676a-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="b676a-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b676a-106">Possible Values</span></span>

<span data-ttu-id="b676a-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b676a-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="b676a-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b676a-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b676a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b676a-109">Remarks</span></span>

<span data-ttu-id="b676a-110">Базовый элемент управления "ползунок" может быть создан путем указания **backgroundColor** или **backgroundImage**, а также **foregroundColor** или **фореграундимаже**.</span><span class="sxs-lookup"><span data-stu-id="b676a-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="b676a-111">При использовании цветов размеры элемента управления Slider определяют область, заполненную цветом фона.</span><span class="sxs-lookup"><span data-stu-id="b676a-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="b676a-112">Цвет переднего плана охватывает цвет фона по мере увеличения положения ползунка.</span><span class="sxs-lookup"><span data-stu-id="b676a-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="b676a-113">Чтобы сделать градиентную заливку области, занятой цветом фона или переднего плана, укажите атрибуты **баккграундендколор** или **фореграундендколор** .</span><span class="sxs-lookup"><span data-stu-id="b676a-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="b676a-114">См. *кустомслидер*. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .</span><span class="sxs-lookup"><span data-stu-id="b676a-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b676a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b676a-115">Requirements</span></span>



| <span data-ttu-id="b676a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b676a-116">Requirement</span></span> | <span data-ttu-id="b676a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b676a-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b676a-118">Версия</span><span class="sxs-lookup"><span data-stu-id="b676a-118">Version</span></span><br/> | <span data-ttu-id="b676a-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b676a-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b676a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b676a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b676a-121">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="b676a-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="b676a-122">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="b676a-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="b676a-123">**ПОЛЗУНок. Баккграундендколор**</span><span class="sxs-lookup"><span data-stu-id="b676a-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="b676a-124">**ПОЛЗУНок. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="b676a-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="b676a-125">**ПОЛЗУНок. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="b676a-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="b676a-126">**ПОЛЗУНок. Фореграундендколор**</span><span class="sxs-lookup"><span data-stu-id="b676a-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="b676a-127">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="b676a-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





