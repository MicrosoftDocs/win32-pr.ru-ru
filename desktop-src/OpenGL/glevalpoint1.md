---
title: Функция glEvalPoint1 (GL. h)
description: Функции glEvalPoint1 и glEvalPoint2 создают и оценивают единую точку в сетке. | Функция glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- Функция glEvalPoint1 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db152c34f9ff3a9b5ad0d157507750302c73f066b32d289cadec4f117485dbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081494"
---
# <a name="glevalpoint1-function"></a>Функция glEvalPoint1

Функции [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2** создают и оценивают единую точку в сетке.

## <a name="syntax"></a>Синтаксис


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*i* 
</dt> <dd>

Целочисленное значение для переменной домена сетки *i*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 





