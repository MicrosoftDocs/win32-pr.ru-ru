---
description: Получение маркера параметра элемента массива.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Метод ID3DXBaseEffect:: Жетпараметерелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355873"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>Метод ID3DXBaseEffect:: Жетпараметерелемент

Получение маркера параметра элемента массива.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер массива. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Елементиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс элемента массива.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер указанного параметра или **значение NULL** , если значение Хпараметер или елементиндекс недопустимо. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Комментарии

Этот метод используется для получения элемента параметра, который является массивом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
