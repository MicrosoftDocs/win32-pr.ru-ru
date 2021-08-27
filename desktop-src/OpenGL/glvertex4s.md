---
title: Функция glVertex4s (GL. h)
description: Указывает вершину. | Функция glVertex4s (GL. h)
ms.assetid: 5030e0dd-9a81-482d-8d87-bfc9355a3c92
keywords:
- Функция glVertex4s OpenGL
topic_type:
- apiref
api_name:
- glVertex4s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53eb5f3270630946c05201c64da5789a79163015dbf3441168f0404411f3782a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035504"
---
# <a name="glvertex4s-function"></a>Функция glVertex4s

Указывает вершину.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glVertex4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*x* 
</dt> <dd>

Задает координату x вершины.

</dd> <dt>

*y* 
</dt> <dd>

Указывает координату y вершины.

</dd> <dt>

*гармошкой* 
</dt> <dd>

Задает z-координату вершины.

</dd> <dt>

*w* 
</dt> <dd>

Задает w-координату вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Команды функции глвертекс используются в парах [**глбегин**](glbegin.md) / [**гленд**](glend.md) для указания вершин, линий и многоугольников. Текущие координаты цвета, нормали и текстуры связаны с вершиной при вызове Глвертекс. Если указаны только значения *x* и *y* , по умолчанию для *z* используется значение 0,0, а для параметров *w* — 1,0. При указании *x*, *y* и *z* значение *w* по умолчанию равно 1,0. Вызов глвертекс за пределами пары **глбегин** / **гленд** приводит к неопределенному поведению.

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

[**глбегин**](glbegin.md)
</dt> <dt>

[**глкалллист**](glcalllist.md)
</dt> <dt>

[**глколор**](glcolor-functions.md)
</dt> <dt>

[**гледжефлаг**](gledgeflag-functions.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глевалкурд**](glevalcoord-functions.md)
</dt> <dt>

[**глиндекс**](glindex-functions.md)
</dt> <dt>

[**глматериал**](glmaterial-functions.md)
</dt> <dt>

[**глнормал**](glnormal-functions.md)
</dt> <dt>

[**глрект**](glrect-functions.md)
</dt> <dt>

[**глтекскурд**](gltexcoord-functions.md)
</dt> </dl>

 

 





