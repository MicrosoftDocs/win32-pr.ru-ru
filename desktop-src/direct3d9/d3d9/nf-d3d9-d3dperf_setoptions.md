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
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805739"
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