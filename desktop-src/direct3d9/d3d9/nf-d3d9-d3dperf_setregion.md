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
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "105719115"
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

## <a name="remarks"></a>Комментарии

Чтобы упростить анализ, Целевая программа может использовать цвет для пометки каждого уровня целевой программы.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |