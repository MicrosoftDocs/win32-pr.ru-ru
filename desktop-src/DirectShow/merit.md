---
description: Значения, определяющие порядок, в котором диспетчер графов фильтров пытается добавить фильтры во время построения графа.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: О-в (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674782"
---
# <a name="merit"></a><span data-ttu-id="82445-103">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="82445-103">Merit</span></span>

<span data-ttu-id="82445-104">Значения, определяющие порядок, в котором диспетчер графов фильтров пытается добавить фильтры во время построения графа.</span><span class="sxs-lookup"><span data-stu-id="82445-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="82445-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Неуспешный \_ Рекомендуемый** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ нормальный** (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_** <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ недоступен \_** (0x400000) не использовать (0x200000) нештатный компрессор (0x100000), которому не удается выполнить <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ \_** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ аппаратный \_ компрессор** (0x100050)</span><span class="sxs-lookup"><span data-stu-id="82445-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="82445-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82445-106">Remarks</span></span>

<span data-ttu-id="82445-107">Каждый фильтр регистрируется со значением, которое заслуживает.</span><span class="sxs-lookup"><span data-stu-id="82445-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="82445-108">Когда диспетчер графов фильтров строит граф, он перечисляет все фильтры, зарегистрированные с правильным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="82445-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="82445-109">Затем он попытается выполнить их в порядке их следования, от самого высокого до самого низкого.</span><span class="sxs-lookup"><span data-stu-id="82445-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="82445-110">(Для выбора фильтров с одинаковым соответствием используются дополнительные критерии). Он никогда не попытается **\_ \_ \_ использовать** фильтры со значением недостижимости, которое меньше или равно ему.</span><span class="sxs-lookup"><span data-stu-id="82445-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="82445-111">Фильтр, который никогда не должен учитываться при обычном воспроизведении, должен **быть \_ \_ не \_ использован** или меньше.</span><span class="sxs-lookup"><span data-stu-id="82445-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="82445-112">Фильтры могут быть зарегистрированы с промежуточными значениями, не определенными этим перечислением, например с недопустимым **\_ нормальным** + 1.</span><span class="sxs-lookup"><span data-stu-id="82445-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="82445-113">Требования</span><span class="sxs-lookup"><span data-stu-id="82445-113">Requirements</span></span>



| <span data-ttu-id="82445-114">Требование</span><span class="sxs-lookup"><span data-stu-id="82445-114">Requirement</span></span> | <span data-ttu-id="82445-115">Значение</span><span class="sxs-lookup"><span data-stu-id="82445-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82445-116">Header</span><span class="sxs-lookup"><span data-stu-id="82445-116">Header</span></span><br/> | <dl> <span data-ttu-id="82445-117"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="82445-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82445-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82445-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82445-119">Константы и идентификаторы GUID</span><span class="sxs-lookup"><span data-stu-id="82445-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="82445-120">Рекомендации по регистрации фильтров</span><span class="sxs-lookup"><span data-stu-id="82445-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="82445-121">Интеллектуальное подключение</span><span class="sxs-lookup"><span data-stu-id="82445-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




