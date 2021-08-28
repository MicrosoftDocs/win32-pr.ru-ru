---
title: Функция Глукуадрикориентатион (GLU. h)
description: Функция Глукуадрикориентатион Указывает ориентацию внутри или снаружи для куадрикс.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- Функция Глукуадрикориентатион OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937630"
---
# <a name="gluquadricorientation-function"></a>Функция Глукуадрикориентатион

Функция **глукуадрикориентатион** Указывает ориентацию внутри или снаружи для куадрикс.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*куадобжект* 
</dt> <dd>

Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).

</dd> <dt>

*ориентация* 
</dt> <dd>

Желаемая ориентация. Допустимы следующие значения.



| Значение                                                                                                                                                   | Значение                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ снаружи**</dt> </dl> | Нарисуйте куадрикс с обычными, указывающими наружу. Это значение по умолчанию.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ внутри**</dt> </dl>    | Нарисуйте куадрикс с обычными, указывающими.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функция **глукуадрикориентатион** указывает, какой вид ориентации требуется для куадрикс, отображаемого с помощью **куадобжект**. Интерпретация наружной и обратной части зависит от прорисовки куадрик.

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

[**глуневкуадрик**](glunewquadric.md)
</dt> <dt>

[**глукуадрикдравстиле**](gluquadricdrawstyle.md)
</dt> <dt>

[**глукуадрикнормалс**](gluquadricnormals.md)
</dt> <dt>

[**глукуадриктекстуре**](gluquadrictexture.md)
</dt> </dl>

 

 





