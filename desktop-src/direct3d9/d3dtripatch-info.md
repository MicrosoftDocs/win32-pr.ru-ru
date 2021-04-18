---
description: Описывает треугольное обновление высокого порядка.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Структура D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713878"
---
# <a name="d3dtripatch_info-structure"></a>\_Структура сведений о D3DTRIPATCH

Описывает треугольное обновление высокого порядка.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**стартвертексоффсет**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальное смещение вершины в количестве вершин.

</dd> <dt>

**нумвертицес**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число вершин.

</dd> <dt>

**База**
</dt> <dd>

Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Член перечисляемого типа [**D3DBASISTYPE**](./d3dbasistype.md) , который определяет тип базиса для треугольного высококачественного исправления. Единственным допустимым значением для этого элемента является D3DBASIS \_ Безье.

</dd> <dt>

**Градус**
</dt> <dd>

Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Элемент перечисляемого типа [**D3DDEGREETYPE**](./d3ddegreetype.md) , определяющий тип степени для треугольного исправления высокого порядка.



| Значение                | Число вершин |
|----------------------|--------------------|
| D3DDEGREE \_ кубический     | 10                 |
| \_Линейная D3DDEGREE    | 3                  |
| D3DDEGREE, \_ квадрат | Н/Д                |
| D3DDEGREE \_ куинтик   | 21                 |



 

Н/д — недоступно. Не поддерживается.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Например, на следующей схеме определяются порядок вершин и номера сегментов для исправления треугольника Безье третьего порядка. Порядок вершин определяет номера сегментов, используемые [**дравтрипатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch). Смещение — это число байтов для первого вершинного исправления треугольника в буфере вершин.

![Схема треугольного исправления высокого порядка с девятью вершинами](images/hop-tripatch-info.png)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**дравтрипатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
