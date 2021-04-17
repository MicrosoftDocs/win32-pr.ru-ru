---
title: Функция glNormal3bv (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3bv (GL. h)
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- Функция glNormal3bv OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d758c1768425ecb736096d59a49133ff4c8918c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684913"
---
# <a name="glnormal3bv-function"></a>Функция glNormal3bv

Задает текущий вектор нормали.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*3,3* 
</dt> <dd>

Указатель на массив из трех элементов: координаты x, y и z нового текущего нормального значения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3bv**.

Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с помощью линейного сопоставления, которое сопоставляет наиболее положительное целочисленное значение 1,0 и самое отрицательное целочисленное значение с-1,0.

Нормали, заданные с помощью **glNormal3bv** , не должны иметь длину единицы. Если нормализация включена, то нормали, заданные с помощью **glNormal3bv** , нормализованы после преобразования. Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации. По умолчанию нормализация отключена. Текущие нормальные обновления можно обновлять в любое время. В частности, можно вызвать **glNormal3bv** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md). Следующие функции извлекают сведения, относящиеся к **glNormal3bv**:

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

 

 





