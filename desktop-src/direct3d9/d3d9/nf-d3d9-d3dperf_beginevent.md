---
title: Функция D3DPERF_BeginEvent
description: Помечает начало определяемого пользователем события. PIX может использовать это событие для активации действия.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412645"
---
# <a name="d3dperf_beginevent-function"></a>Функция D3DPERF_BeginEvent

Помечает начало определяемого пользователем события. PIX может использовать это событие для активации действия.

## <a name="syntax"></a>Синтаксис

```cpp
int WINAPI D3DPERF_BeginEvent(
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

Отсчитываемый от нуля уровень иерархии, в которой начинается это событие. При возникновении ошибки возвращаемое значение будет отрицательным.

## <a name="remarks"></a>Комментарии

Определяемые пользователем события группируют вместе другие события таким образом, чтобы их можно было лучше представить в средствах профилирования производительности. Например, событие *прорисовки пробела* может быть заключено в скобки с несколькими вызовами Direct3D, которые обрисуют место игры. События могут быть вложенными.

Каждый вызов **D3DPERF_BeginEvent** должен иметь соответствующий вызов **D3DPERF_EndEvent** . Мгновенные события (которые не обозначают другие события) должны быть помечены с помощью **D3DPERF_SetMarker** , а не **D3DPERF_BeginEvent** и **D3DPERF_EndEvent**.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |