---
description: Возвращает целое число.
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: 'Метод ID3DXBaseEffect:: GetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6ccd892a7563d4fce300f177a63f5e0cb82601e711f7046e9b9475977409926b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296770"
---
# <a name="id3dxbaseeffectgetint-method"></a>Метод ID3DXBaseEffect:: GetInt

Возвращает целое число.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PN* \[ заполняет\]
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)\***

Возвращает целое число.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetInt**](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 
