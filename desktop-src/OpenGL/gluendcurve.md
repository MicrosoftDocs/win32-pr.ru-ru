---
title: Функция Глуендкурве (GLU. h)
description: Функции Глубегинкурве и Глуендкурве разделяют неоднородное рациональное определение кривой B-сплайна (НУРБС). | Функция Глуендкурве (GLU. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- Функция Глуендкурве OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b6d8e9871b03286eebc285d2c3ad8834c8c354b196213c985626fc80cd02fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489524"
---
# <a name="gluendcurve-function"></a>Функция Глуендкурве

Функции [**глубегинкурве**](glubegincurve.md) и **глуендкурве** разделяют неоднородное рациональное определение кривой B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нобж* 
</dt> <dd>

Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Используйте [**глубегинкурве**](glubegincurve.md) , чтобы пометить начало определения кривой нурбс. После вызова **глубегинкурве** выполните один или несколько вызовов [**глунурбскурве**](glunurbscurve.md) , чтобы определить атрибуты кривой. Ровно один из вызовов **глунурбскурве** должен иметь тип кривой GL \_ «Карта1» \_ Vertex \_ 3 или GL \_ «Карта1» \_ вершиной \_ 4. Чтобы отметить конец определения кривой НУРБС, вызовите **глуендкурве**.

Оценщики OpenGL используются для отрисовки кривой НУРБС в виде ряда сегментов линии. Состояние оценщика сохраняется во время подготовки к просмотру с помощью [**глпушаттриб**](glpushattrib.md) ( \_ бит оценки GL \_ ) и [**глпопаттриб**](glpopattrib.md). Сведения о том, какое состояние эти вызовы сохраняют, см. в разделе **глпушаттриб**.

## <a name="examples"></a>Примеры

Следующие функции визуализируются с помощью текстурной НУРБС кривой с нормальными. координаты текстуры и нормали также указываются в виде кривых НУРБС:

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**глпушаттриб**](glpushattrib.md)
</dt> <dt>

[**глубегинсурфаце**](glubeginsurface.md)
</dt> <dt>

[**глубегинтрим**](glubegintrim.md)
</dt> <dt>

[**глуневнурбсрендерер**](glunewnurbsrenderer.md)
</dt> <dt>

[**глунурбскурве**](glunurbscurve.md)
</dt> </dl>

 

 





