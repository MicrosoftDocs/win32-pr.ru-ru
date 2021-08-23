---
title: Функция D3DPERF_SetRegion
description: Пометьте ряд кадров с указанными цветом и именем в файле Пиксрун. Эта функция в настоящее время не поддерживается PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989264"
---
# <a name="d3dperf_setregion-function"></a>Функция D3DPERF_SetRegion

Пометьте ряд кадров с указанными цветом и именем в файле Пиксрун. Эта функция в настоящее время не поддерживается PIX.

## <a name="syntax"></a>Синтаксис

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Параметры

`col`

Цвет события. Это цвет для отображения события в представлении событий.

`wszName`

Имя события.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы упростить анализ, Целевая программа может использовать цвет для пометки каждого уровня целевой программы.

## <a name="requirements"></a>Requirements (Требования)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |