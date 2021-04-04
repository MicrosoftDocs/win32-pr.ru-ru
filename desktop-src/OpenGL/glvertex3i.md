---
title: Функция glVertex3i (GL. h)
description: Указывает вершину. | Функция glVertex3i (GL. h)
ms.assetid: 5f757065-cbe9-401a-855b-f0a9308ae204
keywords:
- Функция glVertex3i OpenGL
topic_type:
- apiref
api_name:
- glVertex3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e216c35a354daead228d6043d2129f6d30d400
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000104"
---
# <a name="glvertex3i-function"></a>Функция glVertex3i

Указывает вершину.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glVertex3i(
   GLint x,
   GLint y,
   GLint z
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Команды функции глвертекс используются в парах [**глбегин**](glbegin.md) / [**гленд**](glend.md) для указания вершин, линий и многоугольников. Текущие координаты цвета, нормали и текстуры связаны с вершиной при вызове Глвертекс. Если указаны только значения *x* и *y* , по умолчанию для *z* используется значение 0,0, а для параметров *w* — 1,0. При указании *x*, *y* и *z* значение *w* по умолчанию равно 1,0. Вызов глвертекс за пределами пары **глбегин** / **гленд** приводит к неопределенному поведению.

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

 

 





