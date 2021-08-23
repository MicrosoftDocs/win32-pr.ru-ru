---
title: Функция Глуделетекуадрик (GLU. h)
description: Функция Глуделетекуадрик уничтожает объект куадрик.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- Функция Глуделетекуадрик OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c12bd77d3d8b7f7de641671916bb8a901d29d812dfa4e9af6ef116984a128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519624"
---
# <a name="gludeletequadric-function"></a>Функция Глуделетекуадрик

Функция **глуделетекуадрик** уничтожает объект куадрик.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*state* 
</dt> <dd>

Объект куадрик для уничтожения (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функция **глуделетекуадрик** уничтожает объект куадрик и освобождает используемую память. После вызова **глуделетекуадрик** *состояние* нельзя использовать снова.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глуневкуадрик**](glunewquadric.md)
</dt> </dl>

 

 





