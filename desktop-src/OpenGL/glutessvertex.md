---
title: Функция Глутессвертекс (GLU. h)
description: Функция Глутессвертекс указывает вершину многоугольника.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- Функция Глутессвертекс OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3b1dd666fd965e7b6536a20a794481c534ed3e42594017093ee161a067e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488424"
---
# <a name="glutessvertex-function"></a>Функция Глутессвертекс

Функция **глутессвертекс** указывает вершину многоугольника.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тесс* 
</dt> <dd>

Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).

</dd> <dt>

*coords* 
</dt> <dd>

Расположение вершины.

</dd> <dt>

*data* 
</dt> <dd>

Указатель, передаваемый обратно в программу с обратным вызовом вершины (как указано в [*глутесскаллбакк*](glutess.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функция **глутессвертекс** описывает вершину многоугольника, определяемого пользователем. Последовательные вызовы **глутессвертекс** описывают закрытый профиль. Например, чтобы описать грани четырехсторонней, вызовите **глутессвертекс** четыре раза. **Глутессвертекс** можно вызывать только между [**глутессбегинконтаур**](glutessbegincontour.md) и [**глутессендконтаур**](glutessendcontour.md).

Параметр *данных* обычно указывает на структуру, содержащую расположение вершины, а также на другие атрибуты для каждой вершины, такие как цвет и обычный. Этот указатель передается обратно в программу через \_ обратный вызов вершины Glu после тесселяции (см. [*глутесскаллбакк*](glutess.md)).

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

[**глуневтесс**](glunewtess.md)
</dt> <dt>

[**глутессбегинконтаур**](glutessbegincontour.md)
</dt> <dt>

[**глутессбегинполигон**](glubeginpolygon.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> <dt>

[**глутессендконтаур**](glutessendcontour.md)
</dt> <dt>

[**глутесснормал**](glutessnormal.md)
</dt> <dt>

[**глутесспроперти**](glutessproperty.md)
</dt> </dl>

 

 





