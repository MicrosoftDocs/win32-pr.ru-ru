---
title: Функция D3DPERF_GetStatus
description: Определите текущее состояние профилировщика из целевой программы.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805749"
---
# <a name="d3dperf_getstatus-function"></a>Функция D3DPERF_GetStatus

Определите текущее состояние профилировщика из целевой программы.

## <a name="syntax"></a>Синтаксис

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, когда PIX проведет профилирование целевой программы; в противном случае — нуль.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |