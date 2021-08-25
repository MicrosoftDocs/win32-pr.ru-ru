---
description: Описывает прямоугольное исправление высокого порядка.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Структура D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b73ebc548031fd931cce0d34edfadf81a73d71d60edf649718875c52cfc992f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850233"
---
# <a name="d3drectpatch_info-structure"></a>\_Структура сведений о D3DRECTPATCH

Описывает прямоугольное исправление высокого порядка.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**стартвертексоффсетвидс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальная ширина смещения вершины в количестве вершин.

</dd> <dt>

**стартвертексоффсесеигхт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальная высота смещения вершины, в количестве вершин.

</dd> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина каждой вершины в количестве вершин.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота каждой вершины в количестве вершин.

</dd> <dt>

**Stride**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина мнимого двумерного массива вершин, который занимает то же пространство, что и буфер вершин. Пример см. на приведенной ниже схеме.

</dd> <dt>

**База**
</dt> <dd>

Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Элемент перечисляемого типа [**D3DBASISTYPE**](./d3dbasistype.md) , определяющий тип базиса для прямоугольного исправления высокого порядка.



| Значение                 | Поддерживаемые заказы            | Ширина и высота                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ Безье      | Линейный, кубический и куинтик | Width = height = (DWORD) порядок + 1 |
| D3DBASIS \_ бсплине     | Линейный, кубический и куинтик | Width = высота > (DWORD)  |
| D3DBASIS \_ интерполяция | Кривой                      | Width = высота > (DWORD)  |



 

</dd> <dt>

**Градус**
</dt> <dd>

Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Член перечисляемого типа [**D3DDEGREETYPE**](./d3ddegreetype.md) , определяющий степень прямоугольного исправления.

</dd> </dl>

## <a name="remarks"></a>Remarks

На следующей схеме указываются параметры, определяющие обновление прямоугольника.

![Схема прямоугольного исправления высокого порядка и параметров, которые его задают](images/hop-rectpatch.png)

Каждая вершина в буфере вершин отображается в виде черной точки. В этом случае в буфере вершин имеется 20 вершин, 16 из которых находятся в области обновления прямоугольника. Шаг — это число вершин в ширине буфера вершин, в данном случае пять. Смещение x к первой вершине называется Стартиндексвертексвидс и в данном случае равно 1. Смещение y к первой вершине исправления называется Стартиндексвертексхеигхт и в данном случае 0.

Для отображения потока отдельных прямоугольных исправлений (не мозаики) необходимо интерпретировать геометрию как длинное частное (1 x N) прямоугольное исправление. Структура **\_ сведений о D3DRECTPATCH** для такого полоска (кубический Безье) будет настроена следующим образом.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**дравректпатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
