---
description: Возвращает указатель на массив констант в таблице констант.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'Метод ID3DXTextureShader:: Жетконстантдеск (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8c7f65c9f2096339e0131d5d54c2fd65fb7e52849219f06f6a60fd44c518751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095674"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>Метод ID3DXTextureShader:: Жетконстантдеск

Возвращает указатель на массив констант в таблице констант.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор константы. См. [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*пдеск* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Возвращает указатель на массив описаний. См. [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указанный вход должен быть максимальным размером массива. Выходные данные — это количество элементов, заполняемых в массиве при возврате функции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

В таблице константы пробы могут появляться более одного раза, поэтому этот метод может возвращать массив описаний с разными индексами регистров.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader:: DESC**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
