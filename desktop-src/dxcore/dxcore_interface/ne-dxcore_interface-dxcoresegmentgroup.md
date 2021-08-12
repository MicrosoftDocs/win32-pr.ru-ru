---
title: DXCoreSegmentGroup
description: Определяет константы, указывающие группирование сегмента памяти адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279626"
---
# <a name="dxcoresegmentgroup-enum"></a>Перечисление Дкскоресегментграуп

Определяет константы, указывающие группирование сегмента памяти адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Константы

### <a name="local"></a>Local

Указывает группировку сегментов, которые считаются локальными для адаптера, и представляет самый быстрый объем памяти, доступной GPU. Приложение должно ориентироваться на локальную группу сегментов в качестве целевого размера для рабочего набора.

### <a name="nonlocal"></a>Нелокальное

Указывает группу сегментов, которые считаются нелокальными для адаптера и могут иметь более низкую производительность, чем локальная группа сегментов.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)