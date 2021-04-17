---
description: Задает число с плавающей запятой.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'Метод ID3DXConstantTable:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694185"
---
# <a name="id3dxconstanttablesetfloat-method"></a>Метод ID3DXConstantTable:: SetFloat

Задает число с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.

</dd> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор константы. См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*f* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Число с плавающей запятой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
