---
title: Функция Глукуадрикнормалс (GLU. h)
description: Функция Глукуадрикнормалс указывает, какие нормали будут использоваться для куадрикс.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- Функция Глукуадрикнормалс OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491910"
---
# <a name="gluquadricnormals-function"></a>Функция Глукуадрикнормалс

Функция **глукуадрикнормалс** указывает, какие нормали будут использоваться для куадрикс.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*куадобжект* 
</dt> <dd>

Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).

</dd> <dt>

*Normals* 
</dt> <dd>

Требуемый тип нормалй. Допустимы следующие значения.



| Значение                                                                                                                                                | Значение                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ None**</dt> </dl>       | Нормали не создаются.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ бемоль**</dt> </dl>       | Для каждого аспекта куадрик создается один нормальный.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**GLU \_ гладкий**</dt> </dl> | Для каждой вершины куадрик создается один нормальный. Это значение по умолчанию.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция **глукуадрикнормалс** указывает, какие нормали должны использоваться для куадрикс, отображаемого с помощью **куадобжект**.

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

[**глуневкуадрик**](glunewquadric.md)
</dt> <dt>

[**глукуадрикдравстиле**](gluquadricdrawstyle.md)
</dt> <dt>

[**глукуадрикориентатион**](gluquadricorientation.md)
</dt> <dt>

[**глукуадриктекстуре**](gluquadrictexture.md)
</dt> </dl>

 

 





