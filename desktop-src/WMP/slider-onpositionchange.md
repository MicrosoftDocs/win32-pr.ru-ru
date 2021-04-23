---
title: ПОЛЗУНок. Онпоситиончанже
description: Обработчик событий Онпоситиончанже обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем. | ПОЛЗУНок. Онпоситиончанже
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- ПОЛЗУНок. Онпоситиончанже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698833"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="8c410-105">ПОЛЗУНок. Онпоситиончанже</span><span class="sxs-lookup"><span data-stu-id="8c410-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="8c410-106">Обработчик событий **онпоситиончанже** обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.</span><span class="sxs-lookup"><span data-stu-id="8c410-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="8c410-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c410-107">Remarks</span></span>

<span data-ttu-id="8c410-108">Если положение ползунка изменяется в результате изменения атрибута **значения** в скрипте, это событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="8c410-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="8c410-109">Чтобы справиться с этой возможностью, реализуйте вместо него обработчик события **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="8c410-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c410-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8c410-110">Requirements</span></span>



| <span data-ttu-id="8c410-111">Требование</span><span class="sxs-lookup"><span data-stu-id="8c410-111">Requirement</span></span> | <span data-ttu-id="8c410-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8c410-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8c410-113">Версия</span><span class="sxs-lookup"><span data-stu-id="8c410-113">Version</span></span><br/> | <span data-ttu-id="8c410-114">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="8c410-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c410-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c410-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c410-116">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="8c410-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





