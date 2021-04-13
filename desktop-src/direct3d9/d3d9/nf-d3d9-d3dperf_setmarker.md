---
title: Функция D3DPERF_SetMarker
description: Отметить мгновенное событие. PIX может использовать это событие для активации действия.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "104412646"
---
# <a name="d3dperf_setmarker-function"></a>Функция D3DPERF_SetMarker

Отметить мгновенное событие. PIX может использовать это событие для активации действия.

## <a name="syntax"></a>Синтаксис

```cpp
void WINAPI D3DPERF_SetMarker(
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

Мгновенные события пользователя не имеют круглых скобок и не группируют другие события. Например, когда пользователь запускает оружия в игре, событие « *снимок* » может быть создано **D3DPERF_SetMarkerным** вызовом. Чтобы сгруппировать несколько событий под одним, определяемым пользователем именем, используйте **D3DPERF_BeginEvent** и **D3DPERF_EndEvent** , а не **D3DPERF_SetMarker**.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |