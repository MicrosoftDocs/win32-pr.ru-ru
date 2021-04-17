---
description: Возвращает сведения о материалах, сохраненные в файлах Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Структура D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703647"
---
# <a name="d3dxmaterial-structure"></a>Структура D3DXMATERIAL

Возвращает сведения о материалах, сохраненные в файлах Direct3D (. x).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Члены

<dl> <dt>

**MatD3D**
</dt> <dd>

Тип: **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

Структура [**D3DMATERIAL9**](d3dmaterial9.md) , описывающая свойства материала.

</dd> <dt>

**птекстурефиленаме**
</dt> <dd>

Тип: **LPSTR**

</dd> <dd>

Указатель на строку, указывающую имя файла текстуры.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Функции [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) и [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) возвращают массив структур **D3DXMATERIAL** , которые определяют цвет материала и название текстуры для каждого материала в сети. Затем приложение требуется для загрузки текстуры.

Тип LPD3DXMATERIAL определяется как указатель на структуру **D3DXMATERIAL** .


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




