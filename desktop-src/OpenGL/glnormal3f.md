---
title: Функция glNormal3f (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3f (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- Функция glNormal3f OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684911"
---
# <a name="glnormal3f-function"></a>Функция glNormal3f

Задает текущий вектор нормали.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*NX* 
</dt> <dd>

Задает координату x для нового текущего вектора нормали.

</dd> <dt>

*Йорк* 
</dt> <dd>

Задает координату y для нового текущего вектора нормали.

</dd> <dt>

*NZ* 
</dt> <dd>

Задает координату z для нового текущего вектора нормали.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3f** .

Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с линейным сопоставлением, которое сопоставляет наиболее положительное целочисленное значение с 1,0 и самое отрицательное целочисленное значение с-1,0.

Нормали, заданные с помощью **glNormal3f** , не должны иметь длину единицы. Если нормализация включена, то нормали, заданные с помощью **glNormal3f** , нормализуются после преобразования. Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации. По умолчанию нормализация отключена. Текущее нормальное состояние можно обновить в любое время. В частности, можно вызвать **glNormal3f** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md). Следующие функции извлекают сведения, относящиеся к **glNormal3f**:

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

 

 





