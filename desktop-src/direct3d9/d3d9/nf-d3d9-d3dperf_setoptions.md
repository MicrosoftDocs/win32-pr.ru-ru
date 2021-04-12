---
title: Функция D3DPERF_SetOptions
description: Задайте параметры профилировщика, указанные в целевой программе.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104487329"
---
# <a name="d3dperf_setoptions-function"></a>Функция D3DPERF_SetOptions

Задайте параметры профилировщика, указанные в целевой программе.

## <a name="syntax"></a>Синтаксис

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Параметры

`dwOptions`

Параметры пользователя, распознаваемые PIX. Задайте значение 1, чтобы уведомить PIX о том, что целевая программа не предоставляет разрешения на профилирование.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |