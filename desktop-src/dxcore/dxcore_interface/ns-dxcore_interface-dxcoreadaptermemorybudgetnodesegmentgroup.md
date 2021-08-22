---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Описывает группу сегментов памяти для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118658"
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

Указывает физический адаптер устройства, для которого запрашиваются сведения о памяти адаптера. Для операции с одним адаптером задайте для этого параметра значение 0. Если имеется несколько узлов адаптеров, задайте для этого индекса узел (физический адаптер устройства), для которого требуется запросить сведения о памяти адаптера (см. раздел [многоадаптеровые системы](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>сегментграуп

Тип: **[дкскоресегментграуп](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Указывает группирование сегмента памяти адаптера, о котором необходимо выполнить запрос.

## <a name="see-also"></a>См. также раздел

[Справочник по Дкскоре](../dxcore-reference.md)

[Перечисление адаптеров с использованием DXCore](../dxcore-enum-adapters.md)

[Системы с несколькими адаптерами](../../direct3d12/multi-engine.md)