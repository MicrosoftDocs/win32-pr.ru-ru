---
description: Атрибут start указывает время начала объекта относительно родительского объекта.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: начальный атрибут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684133"
---
# <a name="start-attribute"></a><span data-ttu-id="b8ee6-103">начальный атрибут</span><span class="sxs-lookup"><span data-stu-id="b8ee6-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="b8ee6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b8ee6-104">\[Deprecated.</span></span> <span data-ttu-id="b8ee6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8ee6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8ee6-106">`start`Атрибут задает время начала объекта относительно родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="b8ee6-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="b8ee6-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b8ee6-107">Possible Values</span></span>

<span data-ttu-id="b8ee6-108">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="b8ee6-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="b8ee6-109">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="b8ee6-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="b8ee6-110">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="b8ee6-110">Leading units can be omitted.</span></span> <span data-ttu-id="b8ee6-111">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="b8ee6-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b8ee6-112">Применение</span><span class="sxs-lookup"><span data-stu-id="b8ee6-112">Applies To</span></span>

<span data-ttu-id="b8ee6-113">[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="b8ee6-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="b8ee6-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8ee6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ee6-115">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="b8ee6-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8ee6-116">**Иамтимелинеобж:: Сетстартстоп**</span><span class="sxs-lookup"><span data-stu-id="b8ee6-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



