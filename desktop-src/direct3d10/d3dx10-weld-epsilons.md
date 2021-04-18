---
description: Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Структура D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713775"
---
# <a name="d3dx10_weld_epsilons-structure"></a>\_ \_ Структура Эпсилон D3DX10ного шва

Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_WELD_EPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Позиция**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Положение

</dd> <dt>

**блендвеигхтс**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Вес смешения

</dd> <dt>

**Обычный**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Норм.

</dd> <dt>

**псизе**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение размера точки

</dd> <dt>

**Отражающее**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение отраженного освещения

</dd> <dt>

**Диффузное**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Рассеянное значение освещения

</dd> <dt>

**текскурд**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Восемь координат текстуры

</dd> <dt>

**Тангенс**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Тангенс

</dd> <dt>

**бинормал**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

бинормал

</dd> <dt>

**тессфактор**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Фактор тесселяции

</dd> </dl>

## <a name="remarks"></a>Комментарии

Тип LPD3DXWeldEpsilons определяется как указатель на структуру D3DXWeldEpsilons.


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
