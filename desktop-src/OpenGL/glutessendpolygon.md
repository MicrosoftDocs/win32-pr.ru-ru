---
title: Функция Глутессендполигон (GLU. h)
description: Функции Глутессбегинполигон и Глутессендполигон разделяют описание многоугольника. | Функция Глутессендполигон (GLU. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- Функция Глутессендполигон OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65102f1627df682508725d46fc5fa299244e767c318382eacaf3585aa4a471e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061552"
---
# <a name="glutessendpolygon-function"></a>Функция Глутессендполигон

Функции [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон** разделяют описание многоугольника.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluTessEndPolygon(
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

Функции [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон** разделяют определение многоугольника нонконвекс. В каждой паре **глутессбегинполигон**  /  **глутессендполигон** включите один или несколько вызовов [**глутессбегинконтаур**](glutessbegincontour.md). В каждом контуре имеется ноль или более вызовов [**глутессвертекс**](glutessvertex.md). Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).

Параметр *\_ данных Polygon* — это указатель на структуру данных, определяемую программистом. Если указаны соответствующие обратные вызовы (см. [*глутесскаллбакк*](glutess.md)), этот указатель возвращается функции обратного вызова или функциям, что делает его удобным способом для хранения информации на многоугольнике.

При вызове **глутессендполигон** многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов. Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).

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

 

 





