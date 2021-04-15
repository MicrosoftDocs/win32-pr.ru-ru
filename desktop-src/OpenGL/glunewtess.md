---
title: Функция Глуневтесс (GLU. h)
description: Функция Глуневтесс создает объект тесселяции.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- Функция Глуневтесс OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661879"
---
# <a name="glunewtess-function"></a>Функция Глуневтесс

Функция **глуневтесс** создает объект тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="remarks"></a>Комментарии

Функция **глуневтесс** создает и возвращает указатель на новый объект тесселяции. Используйте этот объект при вызове функций тесселяции. Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.

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

[**глуделететесс**](gludeletetess.md)
</dt> <dt>

[**глутессбегинполигон**](glubeginpolygon.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> </dl>

 

 





