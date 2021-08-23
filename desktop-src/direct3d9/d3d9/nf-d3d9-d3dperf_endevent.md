---
title: Функция D3DPERF_EndEvent
description: Помечает конец определяемого пользователем события. PIX может использовать это событие для активации действия.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989254"
---
# <a name="d3dperf_endevent-function"></a>Функция D3DPERF_EndEvent

Помечает конец определяемого пользователем события. PIX может использовать это событие для активации действия.

## <a name="syntax"></a>Синтаксис

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Возвращаемое значение

Уровень иерархии, в которой событие завершается. Если возникает ошибка, это значение отрицательно.

## <a name="requirements"></a>Requirements (Требования)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |