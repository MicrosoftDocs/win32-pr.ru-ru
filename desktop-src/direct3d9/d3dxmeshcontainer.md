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
ms.openlocfilehash: 192b60c34c8a15c34a759bda8fd4f3350956003914f40578bd9c5efa54c772df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731670"
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

**Имя**
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

## <a name="remarks"></a>Remarks

Приложение может быть производным от этой структуры для добавления других данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
