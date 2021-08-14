---
description: Структура D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Структура D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: c4405b383e0403326c3cb84f43c97f4c7da826872b62cb21c94b3edb9ef0e475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298293"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a>Структура D3DXSHPRTSPLITMESHCLUSTERDATA

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**увертстарт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальная вершина в пересопоставленный массив вершин.

</dd> <dt>

**увертленгс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество вершин в этом кластере.

</dd> <dt>

**уфацестарт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальный индекс в массиве лиц.

</dd> <dt>

**уфацеленгс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество лиц в этом кластере.

</dd> <dt>

**уклустерстарт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальный индекс в массиве кластера.

</dd> <dt>

**уклустерленгс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество кластеров в этом массиве.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
