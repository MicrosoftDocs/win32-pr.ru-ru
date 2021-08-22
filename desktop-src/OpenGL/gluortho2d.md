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
ms.openlocfilehash: b4a2f0d5fad1a2efb0df0c802dbb2cf51b54ff3e43402c3143bad982009f4f95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488864"
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

## <a name="remarks"></a>Remarks

Функция **gluOrtho2D** устанавливает двухмерную ортогональную область просмотра. Это эквивалентно вызову [**глорсо**](glortho.md) с знеар =-1 и зфар = 1.

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

[**глорсо**](glortho.md)
</dt> <dt>

[**глуперспективе**](gluperspective.md)
</dt> </dl>

 

 





