---
description: 'Метод ID3DXTextureShader:: Сетбул — задает логическое значение.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'Метод ID3DXTextureShader:: Сетбул (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb16cd5199a9f8638a1d50878bc10cbf264fa2ad1bce37ab61e4c312794710ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790414"
---
# <a name="id3dxtextureshadersetbool-method"></a>Метод ID3DXTextureShader:: Сетбул

Задает логическое значение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор константы. См. [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*б* \[ в\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Логическое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
