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
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104336583"
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