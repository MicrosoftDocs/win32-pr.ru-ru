---
title: Функция gluOrtho2D (GLU. h)
description: Функция gluOrtho2D определяет матрицу двухмерной ортогональной проекции.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Функция gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414709"
---
# <a name="gluortho2d-function"></a>Функция gluOrtho2D

Функция **gluOrtho2D** определяет матрицу двухмерной ортогональной проекции.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*слева* 
</dt> <dd>

Координата для левой вертикальной плоскости обрезки.

</dd> <dt>

*Правильно* 
</dt> <dd>

Координата для правой вертикальной плоскости обрезки.

</dd> <dt>

*В начало* 
</dt> <dd>

Координата для верхней горизонтальной плоскости отсечения.

</dd> <dt>

*Нижний* 
</dt> <dd>

Координата для нижней горизонтальной плоскости обрезки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция **gluOrtho2D** устанавливает двухмерную ортогональную область просмотра. Это эквивалентно вызову [**глорсо**](glortho.md) с Near = 1 и FAR = 1.

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

[**глорсо**](glortho.md)
</dt> <dt>

[**глуперспективе**](gluperspective.md)
</dt> </dl>

 

 





