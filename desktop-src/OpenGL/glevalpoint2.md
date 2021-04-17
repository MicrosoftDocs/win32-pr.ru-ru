---
title: Функция glEvalPoint2 (GL. h)
description: Функции glEvalPoint1 и glEvalPoint2 создают и оценивают единую точку в сетке. | Функция glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- Функция glEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684957"
---
# <a name="glevalpoint2-function"></a>Функция glEvalPoint2

Функции [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2** создают и оценивают единую точку в сетке.

## <a name="syntax"></a>Синтаксис


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*i* 
</dt> <dd>

Целочисленное значение для переменной домена сетки *i*.

</dd> <dt>

*б* 
</dt> <dd>

Целочисленное значение для переменной домена сетки *j* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функции [**глмапгрид**](glmapgrid-functions.md) и [**глевалмеш**](glevalmesh-functions.md) используются совместно для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами. **Глевалпоинт** можно использовать для вычисления одной точки сетки в том же гридспаце, которая проходит через **глевалмеш**. Вызов [**glEvalPoint1**](glevalpoint.md) эквивалентен вызову

**glEvalCoord1** (*i* ?*u*  + *u* 1);

where

? *u* = (*u* 2 *u* 1)/*n*

и *n*, *u* 1 и *u* 2 являются аргументами самой последней функции **glMapGrid1** . Одно абсолютное числовое требование заключается в том, что если *я*  =  *n*, то значение, вычисленное из (*i* ?*u* + U1) представляет собой ровно *u* 2.

В двухмерном регистре **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

где *n*, *u* 1, *u* 2, *m*, *v* 1 и *v* 2 являются аргументами самой последней функции **glMapGrid2** . Затем функция **glEvalPoint2** эквивалентна вызову

**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);

Единственными абсолютными числовыми требованиями является то, что если *я* = *n*, то значение, вычисленное из (*i* ?*u*  +  *u* 1) является ровно U2, и если *j*  =  *m*, то значение, вычисленное на основе (*j* ?*v*  +  *v* 1) является ровно *v* 2.

Следующие функции извлекают сведения, относящиеся к [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2**:

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid

**глжет** с аргументом \_ GL \_ MAP2 \_ домен Grid

**глжет** с аргументами \_ \_ сегментами сетки GL «Карта1» \_

**глжет** с аргументами \_ \_ сегментами сетки GL MAP2 \_

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**глевалкурд**](glevalcoord-functions.md)
</dt> <dt>

[**глевалмеш**](glevalmesh-functions.md)
</dt> <dt>

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**глмапгрид**](glmapgrid-functions.md)
</dt> </dl>

 

 





