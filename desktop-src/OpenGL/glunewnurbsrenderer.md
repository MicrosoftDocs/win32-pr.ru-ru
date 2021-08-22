---
title: Функция Глуневнурбсрендерер (GLU. h)
description: Функция Глуневнурбсрендерер создает неравномерный рациональный объект B-сплайна (НУРБС).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- Функция Глуневнурбсрендерер OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089c1a88ac0fe9ac246efd435ae941ba5e66e2412595e4f5f96dc73e85e90478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937799"
---
# <a name="glunewnurbsrenderer-function"></a>Функция Глуневнурбсрендерер

Функция **глуневнурбсрендерер** создает неравномерный рациональный объект B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Синтаксис


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="remarks"></a>Remarks

Функция **глуневнурбсрендерер** создает и возвращает указатель на новый объект нурбс. Используйте этот объект при вызове функций отрисовки НУРБС и управления. Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**глубегинкурве**](glubegincurve.md)
</dt> <dt>

[**глубегинсурфаце**](glubeginsurface.md)
</dt> <dt>

[**глубегинтрим**](glubegintrim.md)
</dt> <dt>

[**глуделетенурбсрендерер**](gludeletenurbsrenderer.md)
</dt> <dt>

[*глунурбскаллбакк*](glunurbs.md)
</dt> <dt>

[**глунурбспроперти**](glunurbsproperty.md)
</dt> </dl>

 

 





