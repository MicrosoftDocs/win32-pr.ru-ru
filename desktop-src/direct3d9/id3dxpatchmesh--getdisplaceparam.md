---
description: Возвращает параметры смещения геометрического объекта сетки.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'Метод ID3DXPatchMesh:: Жетдисплацепарам (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f079e66f20bfd9b2fab673a0f8c2310a9fd85d84fe4e7d0b8c5ad59d1d61e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847454"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>Метод ID3DXPatchMesh:: Жетдисплацепарам

Возвращает параметры смещения геометрического объекта сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Текстура* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Текстура, содержащая данные смещения.

</dd> <dt>

*Минфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Уровень минификации. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Магфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Уровень увеличения. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Уровень фильтра MIP. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Перенос по словам* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Режим переноса адреса текстуры. Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*двлодбиас* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Уровень детализации значения смещения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Карты смещения могут быть только 2D-текстурой. Функции текстурирования игнорируется для неадаптируемой тесселяции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
