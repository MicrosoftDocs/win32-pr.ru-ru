---
description: Описывает параметры, используемые для загрузки текстуры из другой текстуры.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Структура D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720917"
---
# <a name="d3dx10_texture_load_info-structure"></a>\_ \_ \_ Структура сведений о загрузке текстуры D3DX10

Описывает параметры, используемые для загрузки текстуры из другой текстуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**псркбокс**
</dt> <dd>

Тип: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Поле текстуры источника (см [**. \_ поле D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**пдстбокс**
</dt> <dd>

Тип: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Поле текстуры назначения (см [**. \_ поле D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**сркфирстмип**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Исходный текстурный уровень mipmap, см. раздел [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) для получения дополнительных сведений.

</dd> <dt>

**дстфирстмип**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Целевая текстура mipmap уровень. Дополнительные сведения см. в разделе [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .

</dd> <dt>

**нуммипс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число уровней mipmap в исходной текстуре.

</dd> <dt>

**сркфирстелемент**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Первый элемент текстуры источника.

</dd> <dt>

**дстфирстелемент**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Первый элемент текстуры назначения.

</dd> <dt>

**нумелементс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число загружаемых элементов.

</dd> <dt>

**Фильтр**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Параметры фильтрации при интерполяции (см [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md)).

</dd> <dt>

**мипфилтер**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Параметры фильтрации при создании MIP уровней (см [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в вызове [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
