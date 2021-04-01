---
description: Задает параметры упрощения для сетки.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Перечисление D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157179"
---
# <a name="d3dxmeshsimp-enumeration"></a>Перечисление D3DXMESHSIMP

Задает параметры упрощения для сетки.

## <a name="syntax"></a>Синтаксис


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Вершина D3DXMESHSIMP**
</dt> <dd>

Сетка будет упрощена числом вершин, указанным в параметре MinValue.

</dd> <dt>

<span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_ лицо**
</dt> <dd>

Сетка будет упрощена количеством сторон, указанным в параметре MinValue.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 




