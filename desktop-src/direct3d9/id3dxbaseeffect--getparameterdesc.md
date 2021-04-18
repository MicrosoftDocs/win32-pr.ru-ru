---
description: Возвращает описание параметра или заметки.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Метод ID3DXBaseEffect:: Жетпараметердеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694318"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>Метод ID3DXBaseEffect:: Жетпараметердеск

Возвращает описание параметра или заметки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер параметра или заметки. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***

Возвращает описание указанного параметра или заметки. См. [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




