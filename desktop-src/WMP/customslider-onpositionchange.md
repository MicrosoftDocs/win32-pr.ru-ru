---
title: КУСТОМСЛИДЕР. Онпоситиончанже
description: Обработчик событий Онпоситиончанже обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем. | КУСТОМСЛИДЕР. Онпоситиончанже
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Онпоситиончанже
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695067"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="8e956-105">КУСТОМСЛИДЕР. Онпоситиончанже</span><span class="sxs-lookup"><span data-stu-id="8e956-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="8e956-106">Обработчик событий **онпоситиончанже** обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.</span><span class="sxs-lookup"><span data-stu-id="8e956-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="8e956-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e956-107">Remarks</span></span>

<span data-ttu-id="8e956-108">Если положение настраиваемого ползунка изменяется в результате изменения атрибута **значения** в скрипте, это событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="8e956-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="8e956-109">Чтобы справиться с этой возможностью, реализуйте вместо него обработчик события **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="8e956-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e956-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8e956-110">Requirements</span></span>



| <span data-ttu-id="8e956-111">Требование</span><span class="sxs-lookup"><span data-stu-id="8e956-111">Requirement</span></span> | <span data-ttu-id="8e956-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8e956-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8e956-113">Версия</span><span class="sxs-lookup"><span data-stu-id="8e956-113">Version</span></span><br/> | <span data-ttu-id="8e956-114">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="8e956-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e956-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e956-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e956-116">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="8e956-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





