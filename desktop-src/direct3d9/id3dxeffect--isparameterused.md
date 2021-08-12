---
description: Определяет, используется ли параметр методом.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'Метод ID3DXEffect:: Испараметерусед (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 80b0e69ec4f46541840d5b381cd25d056b25240a00a9ae84b0aaf46a79295ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296005"
---
# <a name="id3dxeffectisparameterused-method"></a>Метод ID3DXEffect:: Испараметерусед

Определяет, используется ли параметр методом.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор параметра. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*хтечникуе* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор для метода. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если параметр используется, и возвращает **значение false** , если параметр не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
