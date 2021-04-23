---
description: Атрибут «завершение» задает время окончания объекта относительно родительского объекта.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Атрибут завершения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684121"
---
# <a name="stop-attribute"></a><span data-ttu-id="adb2a-103">Атрибут завершения</span><span class="sxs-lookup"><span data-stu-id="adb2a-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="adb2a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="adb2a-104">\[Deprecated.</span></span> <span data-ttu-id="adb2a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="adb2a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="adb2a-106">`stop`Атрибут задает время окончания объекта относительно родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="adb2a-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="adb2a-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="adb2a-107">Possible Values</span></span>

<span data-ttu-id="adb2a-108">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="adb2a-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="adb2a-109">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="adb2a-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="adb2a-110">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="adb2a-110">Leading units can be omitted.</span></span> <span data-ttu-id="adb2a-111">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="adb2a-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="adb2a-112">Применение</span><span class="sxs-lookup"><span data-stu-id="adb2a-112">Applies To</span></span>

<span data-ttu-id="adb2a-113">[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="adb2a-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="adb2a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb2a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb2a-115">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="adb2a-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="adb2a-116">**Иамтимелинеобж:: Сетстартстоп**</span><span class="sxs-lookup"><span data-stu-id="adb2a-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



