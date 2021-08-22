---
description: Возвращает состояние литерала параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: Метод ID3DXEffectCompiler::-Literal (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d5c4fcb9b4eb3ee102d4e0676985945cfa227aa35cbd939c8dcd5b8d51da4826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493944"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>Метод ID3DXEffectCompiler::

Возвращает состояние литерала параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор параметра. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*плитерал* \[ заполняет\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)\***

Возвращает значение true, если параметр является литералом, и false в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Эти методы изменяют только то, является ли параметр литералом. Чтобы изменить значение параметра, используйте такой метод, как [**ID3DXBaseEffect:: сетбул**](id3dxbaseeffect--setbool.md) или [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Использование и литералы (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: Сетлитерал**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
