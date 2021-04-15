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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412647"
---
# <a name="d3dperf_endevent-function"></a>Функция D3DPERF_EndEvent

Помечает конец определяемого пользователем события. PIX может использовать это событие для активации действия.

## <a name="syntax"></a>Синтаксис

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Возвращаемое значение

Уровень иерархии, в которой событие завершается. Если возникает ошибка, это значение отрицательно.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |