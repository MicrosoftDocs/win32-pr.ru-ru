---
title: Функция Глуендполигон (GLU. h)
description: Функции Глубегинполигон и Глуендполигон разделяют описание многоугольника. | Функция Глуендполигон (GLU. h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- Функция Глуендполигон OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664873"
---
# <a name="gluendpolygon-function"></a>Функция Глуендполигон

\[Функция **глуендполигон** устарела и предоставляется только для обратной совместимости. Функция **глуендполигон** сопоставляется с **глутессендполигон** , за которым следует **глутессендконтаур**.\]

Функции [**глубегинполигон**](glubeginpolygon.md) и **глуендполигон** разделяют описание многоугольника.

## <a name="syntax"></a>Синтаксис


```C++
void gluEndPolygon(
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

## <a name="remarks"></a>Комментарии

Используйте [**глубегинполигон**](glubeginpolygon.md) и **глуендполигон** для разделения определения многоугольника нонконвекс.

1.  Вызовите **глубегинполигон**.
2.  Определите контуры многоугольника, вызвав [**глутессвертекс**](glutessvertex.md) для каждой вершины и [**глунекстконтаур**](glunextcontour.md) , чтобы начать каждый новый профиль.
3.  Вызовите **глуендполигон** , чтобы сообщить об окончании определения.

    После вызова **глуендполигон** многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов. Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).

## <a name="examples"></a>Примеры

В следующем примере описывается грани четырехсторонней с треугольным отверстием:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

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

[**глуневтесс**](glunewtess.md)
</dt> <dt>

[**глунекстконтаур**](glunextcontour.md)
</dt> <dt>

[**глутессбегинконтаур**](glutessbegincontour.md)
</dt> <dt>

[**глутессбегинполигон**](glutessbeginpolygon.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> <dt>

[**глутессвертекс**](glutessvertex.md)
</dt> </dl>

 

 





