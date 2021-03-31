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
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988884"
---
# <a name="glunewnurbsrenderer-function"></a>Функция Глуневнурбсрендерер

Функция **глуневнурбсрендерер** создает неравномерный рациональный объект B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Синтаксис


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="remarks"></a>Комментарии

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

 

 





