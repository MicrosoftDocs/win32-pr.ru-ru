---
title: Функция D3DPERF_QueryRepeatFrame
description: Определите, запрашивает ли профилировщик производительности запрос о повторной отправке текущего кадра в Direct3D для анализа производительности. Эта функция в настоящее время не поддерживается PIX.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751244"
---
# <a name="d3dperf_queryrepeatframe-function"></a>Функция D3DPERF_QueryRepeatFrame

Определите, запрашивает ли профилировщик производительности запрос о повторной отправке текущего кадра в Direct3D для анализа производительности. Эта функция в настоящее время не поддерживается PIX.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Возвращаемое значение

Если возвращаемое значение равно TRUE, вызывающий объект должен повторить ту же последовательность вызовов. Если значение равно FALSE, вызывающий объект должен продолжать работу.

## <a name="remarks"></a>Remarks

Функция должна вызываться сразу после **IDirect3DDevice9::P** вызывается повторная отправка.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | d3d9. h |
| **Библиотека** | d3d9. lib |
| **КОМПОНОВКИ** | d3d9.dll |