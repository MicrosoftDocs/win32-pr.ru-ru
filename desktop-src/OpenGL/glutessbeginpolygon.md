---
title: Функция Глутессбегинполигон (GLU. h)
description: Функции Глутессбегинполигон и Глутессендполигон разделяют описание многоугольника. | Функция Глутессбегинполигон (GLU. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- Функция Глутессбегинполигон OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42566cf8a0674086883e6333a67ac2df03329f6a9bd3bb903ef558af3c430b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777394"
---
# <a name="glutessbeginpolygon-function"></a>Функция Глутессбегинполигон

Функции **глутессбегинполигон** и [**глутессендполигон**](glutessendpolygon.md) разделяют описание многоугольника.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тесс* 
</dt> <dd>

Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).

</dd> <dt>

*данные многоугольника \_* 
</dt> <dd>

Указатель на структуру данных многоугольников, определяемую программистом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функции **глутессбегинполигон** и [**глутессендполигон**](glutessendpolygon.md) разделяют определение многоугольника нонконвекс. В каждой паре **глутессбегинполигон**  /  **глутессендполигон** включите один или несколько вызовов [**глутессбегинконтаур**](glutessbegincontour.md). В каждом контуре имеется ноль или более вызовов [**глутессвертекс**](glutessvertex.md). Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).

Параметр *\_ данных Polygon* — это указатель на структуру данных, определяемую программистом. Если указаны соответствующие обратные вызовы (см. [*глутесскаллбакк*](glutess.md)), этот указатель возвращается функции обратного вызова или функциям, что делает его удобным способом для хранения информации на многоугольнике.

При вызове [**глутессендполигон**](glutessendpolygon.md)многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов. Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).

## <a name="examples"></a>Примеры

Ниже описывается грани четырехсторонней с треугольным отверстием:

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
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

[**глутессбегинконтаур**](glutessbegincontour.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> <dt>

[**глутессендконтаур**](glutessendcontour.md)
</dt> <dt>

[**глутесснормал**](glutessnormal.md)
</dt> <dt>

[**глутесспроперти**](glutessproperty.md)
</dt> <dt>

[**глутессвертекс**](glutessvertex.md)
</dt> </dl>

 

 





