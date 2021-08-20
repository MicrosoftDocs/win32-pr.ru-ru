---
title: Функция Глубегинполигон (GLU. h)
description: Функции Глубегинполигон и Глуендполигон разделяют описание многоугольника. | Функция Глубегинполигон (GLU. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- Функция Глубегинполигон OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98fe58a48a10d36a07e3a96bdfe612d8857f691233e19faac670eb6d987b42f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937897"
---
# <a name="glubeginpolygon-function"></a>Функция Глубегинполигон

\[Функция **глубегинполигон** устарела и предоставляется только для обратной совместимости. Функция **глубегинполигон** сопоставляется с [**глутессбегинполигон**](glutessbeginpolygon.md) , за которым следует [**глутессбегинконтаур**](glutessbegincontour.md).\]

Функции **глубегинполигон** и [**глуендполигон**](gluendpolygon.md) разделяют описание многоугольника.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluBeginPolygon(
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

Используйте **глубегинполигон** и **глуендполигон** для разделения определения многоугольника нонконвекс.

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

 

 





