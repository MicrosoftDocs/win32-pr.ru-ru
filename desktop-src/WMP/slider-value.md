---
title: ПОЛЗУНок. Value
description: Атрибут value указывает или получает текущую точку ползунка. | ПОЛЗУНок. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Windows Media Player с ПОЛЗУНКом. Value
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657269"
---
# <a name="slidervalue"></a><span data-ttu-id="df0dc-105">ПОЛЗУНок. Value</span><span class="sxs-lookup"><span data-stu-id="df0dc-105">SLIDER.value</span></span>

<span data-ttu-id="df0dc-106">Атрибут **value** указывает или получает текущую точку ползунка.</span><span class="sxs-lookup"><span data-stu-id="df0dc-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="df0dc-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="df0dc-107">Possible Values</span></span>

<span data-ttu-id="df0dc-108">Этот атрибут является **числом** для чтения и записи (**float**) и значением по умолчанию **min**.</span><span class="sxs-lookup"><span data-stu-id="df0dc-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="df0dc-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df0dc-109">Remarks</span></span>

<span data-ttu-id="df0dc-110">**Значение** всегда должно быть больше или равно **min** и меньше или равно **Max**. Если указать значение вне этого диапазона, **значение** и положение ползунка не изменяются.</span><span class="sxs-lookup"><span data-stu-id="df0dc-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="df0dc-111">См. **кустомслидер**. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .</span><span class="sxs-lookup"><span data-stu-id="df0dc-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0dc-112">Требования</span><span class="sxs-lookup"><span data-stu-id="df0dc-112">Requirements</span></span>



| <span data-ttu-id="df0dc-113">Требование</span><span class="sxs-lookup"><span data-stu-id="df0dc-113">Requirement</span></span> | <span data-ttu-id="df0dc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="df0dc-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="df0dc-115">Версия</span><span class="sxs-lookup"><span data-stu-id="df0dc-115">Version</span></span><br/> | <span data-ttu-id="df0dc-116">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="df0dc-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df0dc-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df0dc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0dc-118">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="df0dc-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="df0dc-119">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="df0dc-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





