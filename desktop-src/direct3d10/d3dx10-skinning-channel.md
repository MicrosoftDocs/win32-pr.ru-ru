---
description: Член decl в соответствии с тем, для чего выполняется выборка программного обеспечения. Он используется с API ID3DX10SkinInfo::D Ософтварескиннинг.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Структура D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b8e976ba1aecdeb792ba45fc4f60f25e7feb5a7dde3f7fc845a22962e441bf2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753534"
---
# <a name="d3dx10_skinning_channel-structure"></a>\_Структура канала обложки D3DX10 \_

Член decl в соответствии с тем, для чего выполняется выборка программного обеспечения. Он используется с API [**ID3DX10SkinInfo::D ософтварескиннинг**](id3dx10skininfo-dosoftwareskinning.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Члены

<dl> <dt>

**сркоффсет**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала каждой исходной вершины.

</dd> <dt>

**дестоффсет**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала каждой конечной вершины.

</dd> <dt>

**Обычная**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Определяет, какой массив матриц используется в API [**ID3DX10SkinInfo::D ософтварескиннинг**](id3dx10skininfo-dosoftwareskinning.md) . Если это так, будет использоваться *пинверсетранспосебонематрицес* , в противном случае будет использоваться *пбонематрицес* .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
