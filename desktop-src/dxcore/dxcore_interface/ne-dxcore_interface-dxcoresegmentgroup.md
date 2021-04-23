---
title: DXCoreSegmentGroup
description: Определяет константы, указывающие группирование сегмента памяти адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719130"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="5f11d-103">Перечисление Дкскоресегментграуп</span><span class="sxs-lookup"><span data-stu-id="5f11d-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="5f11d-104">Определяет константы, указывающие группирование сегмента памяти адаптера.</span><span class="sxs-lookup"><span data-stu-id="5f11d-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f11d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f11d-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="5f11d-106">Константы</span><span class="sxs-lookup"><span data-stu-id="5f11d-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="5f11d-107">Локальная</span><span class="sxs-lookup"><span data-stu-id="5f11d-107">Local</span></span>

<span data-ttu-id="5f11d-108">Указывает группировку сегментов, которые считаются локальными для адаптера, и представляет самый быстрый объем памяти, доступной GPU.</span><span class="sxs-lookup"><span data-stu-id="5f11d-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="5f11d-109">Приложение должно ориентироваться на локальную группу сегментов в качестве целевого размера для рабочего набора.</span><span class="sxs-lookup"><span data-stu-id="5f11d-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="5f11d-110">Нелокальное</span><span class="sxs-lookup"><span data-stu-id="5f11d-110">NonLocal</span></span>

<span data-ttu-id="5f11d-111">Указывает группу сегментов, которые считаются нелокальными для адаптера и могут иметь более низкую производительность, чем локальная группа сегментов.</span><span class="sxs-lookup"><span data-stu-id="5f11d-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f11d-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f11d-112">See also</span></span>

<span data-ttu-id="5f11d-113">[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="5f11d-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>