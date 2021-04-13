---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Описывает группу сегментов памяти для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413105"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>Структура Дкскореадаптермеморибуджетнодесегментграуп

Описывает группу сегментов памяти для адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Члены

### <a name="nodeindex"></a>нодеиндекс

Тип: **uint32_t**

Указывает физический адаптер устройства, для которого запрашиваются сведения о памяти адаптера. Для операции с одним адаптером задайте для этого параметра значение 0. Если имеется несколько узлов адаптеров, задайте для этого индекса узел (физический адаптер устройства), для которого требуется запросить сведения о памяти адаптера (см. раздел [многоадаптеровые системы](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>сегментграуп

Тип: **[дкскоресегментграуп](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Указывает группирование сегмента памяти адаптера, о котором необходимо выполнить запрос.

## <a name="see-also"></a>См. также раздел

[Справочник по Дкскоре](../dxcore-reference.md)

[Перечисление адаптеров с использованием DXCore](../dxcore-enum-adapters.md)

[Системы с несколькими адаптерами](../../direct3d12/multi-engine.md)