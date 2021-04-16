---
title: ПОЛЗУНок. foregroundColor
description: Атрибут foregroundColor указывает или получает цвет переднего плана для элемента управления "ползунок".
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- ПОЛЗУНок. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657915"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="01c1e-104">ПОЛЗУНок. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="01c1e-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="01c1e-105">Атрибут **foregroundColor** указывает или получает цвет переднего плана для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="01c1e-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="01c1e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="01c1e-106">Possible Values</span></span>

<span data-ttu-id="01c1e-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="01c1e-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="01c1e-108">Значение по умолчанию — "белый".</span><span class="sxs-lookup"><span data-stu-id="01c1e-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="01c1e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01c1e-109">Remarks</span></span>

<span data-ttu-id="01c1e-110">Базовый элемент управления "ползунок" может быть создан путем указания одной из двух пар атрибутов: **backgroundColor** и **foregroundColor**, **backgroundImage** и **фореграундимаже**.</span><span class="sxs-lookup"><span data-stu-id="01c1e-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="01c1e-111">При создании элемента управления "ползунок" с помощью атрибутов цвета размеры элемента управления "ползунок" определяют область, заполненную цветом фона.</span><span class="sxs-lookup"><span data-stu-id="01c1e-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="01c1e-112">Цвет переднего плана охватывает цвет фона по мере увеличения положения ползунка.</span><span class="sxs-lookup"><span data-stu-id="01c1e-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="01c1e-113">Чтобы сделать градиентную заливку в области, занимаемой цветом фона или переднего плана, укажите атрибуты **баккграундендколор** или **фореграундендколор** .</span><span class="sxs-lookup"><span data-stu-id="01c1e-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="01c1e-114">См. *кустомслидер*. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .</span><span class="sxs-lookup"><span data-stu-id="01c1e-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c1e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="01c1e-115">Requirements</span></span>



| <span data-ttu-id="01c1e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="01c1e-116">Requirement</span></span> | <span data-ttu-id="01c1e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="01c1e-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="01c1e-118">Версия</span><span class="sxs-lookup"><span data-stu-id="01c1e-118">Version</span></span><br/> | <span data-ttu-id="01c1e-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="01c1e-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01c1e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01c1e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c1e-121">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="01c1e-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="01c1e-122">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="01c1e-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="01c1e-123">**ПОЛЗУНок. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="01c1e-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="01c1e-124">**ПОЛЗУНок. Баккграундендколор**</span><span class="sxs-lookup"><span data-stu-id="01c1e-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="01c1e-125">**ПОЛЗУНок. Фореграундендколор**</span><span class="sxs-lookup"><span data-stu-id="01c1e-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="01c1e-126">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="01c1e-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





