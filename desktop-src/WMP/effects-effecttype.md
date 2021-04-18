---
title: EFFECTs. Еффекттипе
description: Метод Еффекттипе извлекает имя реестра визуализации с указанным индексом реестра. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- Effect. Еффекттипе Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695036"
---
# <a name="effectseffecttype"></a><span data-ttu-id="64490-105">EFFECTs. Еффекттипе</span><span class="sxs-lookup"><span data-stu-id="64490-105">EFFECTS.effectType</span></span>

<span data-ttu-id="64490-106">Метод **еффекттипе** извлекает имя реестра визуализации с указанным индексом реестра.</span><span class="sxs-lookup"><span data-stu-id="64490-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="64490-107">Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.</span><span class="sxs-lookup"><span data-stu-id="64490-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="64490-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="64490-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64490-109"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="64490-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="64490-110">**Число** (**Long**), содержащее индекс реестра визуализации.</span><span class="sxs-lookup"><span data-stu-id="64490-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64490-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64490-111">Return Value</span></span>

<span data-ttu-id="64490-112">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="64490-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="64490-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64490-113">Remarks</span></span>

<span data-ttu-id="64490-114">Этот метод полезен для переключения между визуализациями в скрипте.</span><span class="sxs-lookup"><span data-stu-id="64490-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="64490-115">Пользовательский интерфейс может отображать набор заголовков, но когда пользователь выбирает его, скрипт должен использовать **куррентеффекттипе** для переключения визуализаций.</span><span class="sxs-lookup"><span data-stu-id="64490-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="64490-116">Требования</span><span class="sxs-lookup"><span data-stu-id="64490-116">Requirements</span></span>



| <span data-ttu-id="64490-117">Требование</span><span class="sxs-lookup"><span data-stu-id="64490-117">Requirement</span></span> | <span data-ttu-id="64490-118">Значение</span><span class="sxs-lookup"><span data-stu-id="64490-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="64490-119">Версия</span><span class="sxs-lookup"><span data-stu-id="64490-119">Version</span></span><br/> | <span data-ttu-id="64490-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="64490-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64490-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64490-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64490-122">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="64490-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="64490-123">**EFFECTs. Куррентеффекттипе**</span><span class="sxs-lookup"><span data-stu-id="64490-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





