---
description: Загрузка текстуры из текстуры.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Функция D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354433"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>Функция D3DX10LoadTextureFromTexture

Загрузка текстуры из текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псрктекстуре* 
</dt> <dd>

Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Указатель на исходную текстуру. См. [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*плоадинфо* 
</dt> <dd>

Тип: **[ **\_ \_ \_ сведения о загрузке текстуры D3DX10**](d3dx10-texture-load-info.md)\***

Указатель на параметры загрузки текстуры. См [**. \_ \_ \_ сведения о загрузке текстур D3DX10**](d3dx10-texture-load-info.md).

</dd> <dt>

*пдсттекстуре* 
</dt> <dd>

Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Указатель на текстуру назначения. См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




