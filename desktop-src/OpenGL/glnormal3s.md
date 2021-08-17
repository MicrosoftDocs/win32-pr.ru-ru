---
title: Функция glNormal3s (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- Функция glNormal3s OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a21ce2ff4c780e19e0849730db5fb7831343a32961e0e673b355124f799c61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795257"
---
# <a name="glnormal3s-function"></a>Функция glNormal3s

Задает текущий вектор нормали.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*NX* 
</dt> <dd>

Задает координату x нового текущего вектора нормали.

</dd> <dt>

*Йорк* 
</dt> <dd>

Задает координату по оси y нового текущего вектора нормали.

</dd> <dt>

*NZ* 
</dt> <dd>

Задает z-координату нового текущего вектора нормали.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3s**.

Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с линейным сопоставлением, которое сопоставляет наиболее положительное целочисленное значение с 1,0 и самое отрицательное целочисленное значение с-1,0.

Нормали, заданные с помощью **glNormal3s** , не должны иметь длину единицы. Если нормализация включена, то нормали, заданные с помощью **glNormal3s** , нормализуются после преобразования. Вы можете управлять нормализатионби с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации. По умолчанию нормализация отключена. Текущее нормальное состояние можно обновить в любое время. В частности, можно вызвать **glNormal3s** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md). Следующие функции извлекают сведения, относящиеся к **glNormal3s**:

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ нормальная

[**глисенабле**](glisenabled.md) с аргументом \_ нормализации GL

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

[**глбегин**](glbegin.md)
</dt> <dt>

[**глколор**](glcolor-functions.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глиндекс**](glindex-functions.md)
</dt> <dt>

[**глтекскурд**](gltexcoord-functions.md)
</dt> <dt>

[**глвертекс**](glvertex-functions.md)
</dt> </dl>

 

 





