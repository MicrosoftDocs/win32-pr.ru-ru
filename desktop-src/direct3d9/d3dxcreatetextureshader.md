---
description: Создает объект шейдера текстуры из скомпилированного шейдера.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Функция D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e989570c98b6b306782d8fb01e53b04d7157b1bb46db726a27fe2ade88a806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298975"
---
# <a name="d3dxcreatetextureshader-function"></a>Функция D3DXCreateTextureShader

Создает объект шейдера текстуры из скомпилированного шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции DWORD.

</dd> <dt>

*пптекстурешадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

Возвращает объект [**ID3DXTextureShader**](id3dxtextureshader.md) , который можно использовать для процедурного заполнения содержимого текстуры с помощью функций [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
