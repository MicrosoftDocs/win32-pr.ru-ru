---
description: Атрибут «выкл.» указывает состояние отключения объекта.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: отключить атрибут
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140251"
---
# <a name="mute-attribute"></a><span data-ttu-id="4d31a-103">отключить атрибут</span><span class="sxs-lookup"><span data-stu-id="4d31a-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="4d31a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4d31a-104">\[Deprecated.</span></span> <span data-ttu-id="4d31a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d31a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d31a-106">`mute`Атрибут указывает состояние отключения объекта.</span><span class="sxs-lookup"><span data-stu-id="4d31a-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="4d31a-107">Если значение равно **true**, то ни объект, ни его дочерние элементы не отображаются.</span><span class="sxs-lookup"><span data-stu-id="4d31a-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="4d31a-108">Если значение равно **false**, объект визуализируется и его дочерние элементы отображаются в соответствии со своим состоянием отключения.</span><span class="sxs-lookup"><span data-stu-id="4d31a-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="4d31a-109">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="4d31a-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="4d31a-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4d31a-110">Possible Values</span></span>

<span data-ttu-id="4d31a-111">Следующие значения определены как TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="4d31a-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="4d31a-112">Следующие значения определены как FALSE: n, N, f, F, 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="4d31a-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4d31a-113">Применение</span><span class="sxs-lookup"><span data-stu-id="4d31a-113">Applies To</span></span>

<span data-ttu-id="4d31a-114">[**клип**](clip-element.md), [**составной**](composite-element.md), [**эффекты**](effect-element.md), [**Группа**](group-element.md), [**временная шкала**](timeline-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="4d31a-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="4d31a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d31a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d31a-116">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="4d31a-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d31a-117">**Иамтимелинеобж:: Сетмутед**</span><span class="sxs-lookup"><span data-stu-id="4d31a-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



