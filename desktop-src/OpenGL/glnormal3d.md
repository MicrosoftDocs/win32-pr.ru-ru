---
title: Функция glNormal3d (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3d (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- Функция glNormal3d OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53eb5950b34b9f3fa838e773f7e3e6438caa603162ca8f8181534e67e8540191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128194"
---
# <a name="glnormal3d-function"></a>Функция glNormal3d

Задает текущий вектор нормали.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
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

## <a name="remarks"></a>Remarks

Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3d**.

Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с помощью линейного сопоставления, которое сопоставляет наиболее положительное целочисленное значение 1,0 и самое отрицательное целочисленное значение с-1,0.

Нормали, заданные с помощью **glNormal3d** , не должны иметь длину единицы. Если нормализация включена, то нормали, заданные с помощью **glNormal3d** , нормализуются после преобразования. Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации. По умолчанию нормализация отключена. Текущее нормальное состояние можно обновить в любое время. В частности, можно вызвать **glNormal3d** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md). Следующие функции извлекают сведения, относящиеся к **glNormal3d**:

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

 

 





