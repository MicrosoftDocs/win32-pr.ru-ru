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

### <a name="local"></a>Локальная

Указывает группировку сегментов, которые считаются локальными для адаптера, и представляет самый быстрый объем памяти, доступной GPU. Приложение должно ориентироваться на локальную группу сегментов в качестве целевого размера для рабочего набора.

### <a name="nonlocal"></a>Нелокальное

Указывает группу сегментов, которые считаются нелокальными для адаптера и могут иметь более низкую производительность, чем локальная группа сегментов.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)