---
description: Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'Метод ID3DXEffect:: Финднекствалидтечникуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424413"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>Метод ID3DXEffect:: Финднекствалидтечникуе

Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хтечникуе* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор для метода. См. раздел [Handles (Direct3D 9)](handles.md). Укажите **значение NULL** для этого параметра, чтобы найти первую допустимую методику.

</dd> <dt>

*птечникуе* \[ заполняет\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Указатель на идентификатор для следующего метода. Если это последний метод, возвращается **значение NULL** . См. раздел [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect:: Валидатетечникуе**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




