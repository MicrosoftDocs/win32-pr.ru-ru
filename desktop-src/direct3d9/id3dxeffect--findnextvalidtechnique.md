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
ms.openlocfilehash: f65a08d1f1ec8a1f7710272d2a1c48e936f211b3bcdee8b84652b9a7196f39e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118704"
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
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect:: Валидатетечникуе**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




