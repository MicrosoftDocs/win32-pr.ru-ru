---
description: Задает трансобъектную матрицу.
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'Метод ID3DXTextureShader:: Сетматрикс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c52fa8d363200222197ac40563fb0dd66e71f7a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157159"
---
# <a name="id3dxtextureshadersetmatrix-method"></a>Метод ID3DXTextureShader:: Сетматрикс

Задает трансобъектную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор матрицы констант. См. [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*пматрикс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на трансобъектную матрицу. См. [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Неперенесенная матрица содержит основные данные строки. то есть каждый вектор содержится в строке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




