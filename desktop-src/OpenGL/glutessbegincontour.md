---
title: Функция Глутессбегинконтаур (GLU. h)
description: Функции Глутессбегинконтаур и Глутессендконтаур разделяют описание контура. | Функция Глутессбегинконтаур (GLU. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- Функция Глутессбегинконтаур OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc46eb3aa1be6b37c9276bcfd1c2b951162722689b0d0affc358a71119736f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937475"
---
# <a name="glutessbegincontour-function"></a>Функция Глутессбегинконтаур

Функции **глутессбегинконтаур** и [**глутессендконтаур**](glutessendcontour.md) разделяют описание контура.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тесс* 
</dt> <dd>

Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функции **глутессбегинконтаур** и [**глутессендполигон**](glutessendpolygon.md) разделяют определение контура многоугольника. Внутри каждой пары **глутессбегинконтаур** / **глутессендполигон** может быть несколько вызовов [**глутессвертекс**](glutessvertex.md). Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым). **Глутессбегинконтаур** можно вызывать только между [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон**.

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

[**глутессбегинполигон**](glutessbeginpolygon.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> <dt>

[**глутессендполигон**](glutessendpolygon.md)
</dt> <dt>

[**глутесснормал**](glutessnormal.md)
</dt> <dt>

[**глутесспроперти**](glutessproperty.md)
</dt> <dt>

[**глутессвертекс**](glutessvertex.md)
</dt> </dl>

 

 





