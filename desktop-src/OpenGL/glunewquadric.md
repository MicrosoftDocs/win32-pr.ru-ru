---
title: Функция Глуневкуадрик (GLU. h)
description: Функция Глуневкуадрик создает объект куадрик.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- Функция Глуневкуадрик OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66fed28c555d327bffa18d8f9100a6f5e9824b714bff1308e6b2dab20b5d3671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036274"
---
# <a name="glunewquadric-function"></a>Функция Глуневкуадрик

Функция **глуневкуадрик** создает объект куадрик.

## <a name="syntax"></a>Синтаксис


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="remarks"></a>Remarks

Функция **глуневкуадрик** создает и возвращает указатель на новый объект куадрик. Используйте этот объект при вызове функций отрисовки куадрик и управления. Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.

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

[**глуцилиндер**](glucylinder.md)
</dt> <dt>

[**глуделетекуадрик**](gludeletequadric.md)
</dt> <dt>

[**глудиск**](gludisk.md)
</dt> <dt>

[**глупартиалдиск**](glupartialdisk.md)
</dt> <dt>

[*глукуадриккаллбакк*](gluquadric.md)
</dt> <dt>

[**глукуадрикдравстиле**](gluquadricdrawstyle.md)
</dt> <dt>

[**глукуадрикнормалс**](gluquadricnormals.md)
</dt> <dt>

[**глукуадрикориентатион**](gluquadricorientation.md)
</dt> <dt>

[**глукуадриктекстуре**](gluquadrictexture.md)
</dt> <dt>

[**глусфере**](glusphere.md)
</dt> </dl>

 

 





