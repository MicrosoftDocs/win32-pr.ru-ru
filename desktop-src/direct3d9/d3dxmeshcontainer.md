---
description: Инкапсулирует объект сетки в иерархии фрейма преобразования.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Структура D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354180"
---
# <a name="d3dxmeshcontainer-structure"></a>Структура D3DXMESHCONTAINER

Инкапсулирует объект сетки в иерархии фрейма преобразования.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Name**
</dt> <dd>

Тип: **LPSTR**

</dd> <dd>

Имя сетки.

</dd> <dt>

**мешдата**
</dt> <dd>

Тип: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Тип данных в сетке. См. [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**пматериалс**
</dt> <dd>

Тип: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Массив материалов для сетки. См. [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**пеффектс**
</dt> <dd>

Тип: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Указатель на набор параметров эффектов по умолчанию. См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**нумматериалс**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число материалов в сетке.

</dd> <dt>

**паджаценци**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Указатель на массив из трех DWORD на треугольник сетки, содержащей сведения о смежности.

</dd> <dt>

**пскининфо**
</dt> <dd>

Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Указатель на интерфейс сведений об обложке. См. [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**пнекстмешконтаинер**
</dt> <dd>

Тип: * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

Указатель на следующий контейнер сетки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Приложение может быть производным от этой структуры для добавления других данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
