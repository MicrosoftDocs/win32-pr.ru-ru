---
description: Атрибут Time указывает время, когда параметр принимает новое значение относительно начала перехода или воздействия.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Атрибут времени
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272965"
---
# <a name="time-attribute"></a><span data-ttu-id="a2df1-103">Атрибут времени</span><span class="sxs-lookup"><span data-stu-id="a2df1-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="a2df1-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a2df1-104">\[Deprecated.</span></span> <span data-ttu-id="a2df1-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2df1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a2df1-106">`time`Атрибут задает время, когда параметр принимает новое значение относительно начала перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="a2df1-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="a2df1-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a2df1-107">Possible Values</span></span>

<span data-ttu-id="a2df1-108">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="a2df1-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="a2df1-109">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="a2df1-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="a2df1-110">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="a2df1-110">Leading units can be omitted.</span></span> <span data-ttu-id="a2df1-111">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="a2df1-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a2df1-112">Применение</span><span class="sxs-lookup"><span data-stu-id="a2df1-112">Applies To</span></span>

<span data-ttu-id="a2df1-113">[**в**](at-element.md), [ **Линейная**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="a2df1-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="a2df1-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2df1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2df1-115">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="a2df1-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



