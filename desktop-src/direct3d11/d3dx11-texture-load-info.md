---
title: Структура D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Описывает параметры, используемые для загрузки текстуры из другой текстуры.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b441ed81e7054cb84731f204ddbf2a863b7a98a75e5e01ed54cf49b28dba7957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989904"
---
# <a name="d3dx11_texture_load_info-structure"></a>\_ \_ \_ Структура сведений о загрузке текстуры D3DX11

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

Описывает параметры, используемые для загрузки текстуры из другой текстуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**псркбокс**
</dt> <dd>

Тип: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Поле текстуры источника (см [**. \_ поле D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**пдстбокс**
</dt> <dd>

Тип: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Поле текстуры назначения (см [**. \_ поле D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**сркфирстмип**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Исходный текстурный уровень mipmap, см. раздел [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) для получения дополнительных сведений.

</dd> <dt>

**дстфирстмип**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Целевая текстура mipmap уровень. Дополнительные сведения см. в разделе [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .

</dd> <dt>

**нуммипс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число уровней mipmap в исходной текстуре.

</dd> <dt>

**сркфирстелемент**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Первый элемент текстуры источника.

</dd> <dt>

**дстфирстелемент**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Первый элемент текстуры назначения.

</dd> <dt>

**нумелементс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число загружаемых элементов.

</dd> <dt>

**Filter**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Параметры фильтрации при интерполяции (см [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md)).

</dd> <dt>

**мипфилтер**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Параметры фильтрации при создании MIP уровней (см [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется в вызове [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

Значения по умолчанию:


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

