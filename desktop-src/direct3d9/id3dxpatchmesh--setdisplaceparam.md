---
description: Задает параметры смещения геометрических объектов сетки.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'Метод ID3DXPatchMesh:: Сетдисплацепарам (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664986"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a>Метод ID3DXPatchMesh:: Сетдисплацепарам

Задает параметры смещения геометрических объектов сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Текстура* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Текстура, содержащая данные смещения.

</dd> <dt>

*Минфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Уровень минификации. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Магфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Уровень увеличения. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Уровень фильтра MIP. Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Перенос по словам* \[ окне\]
</dt> <dd>

Тип: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**

Режим переноса адреса текстуры. Дополнительные сведения см. в разделе [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)

</dd> <dt>

*двлодбиас* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Уровень детализации значения смещения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Карты смещения могут быть только 2D-текстурой. Функции текстурирования игнорируется для неадаптируемой тесселяции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
