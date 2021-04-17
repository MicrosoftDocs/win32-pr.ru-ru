---
description: Возвращает описание функции.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Метод ID3DXBaseEffect:: Жетфунктиондеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703994"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>Метод ID3DXBaseEffect:: Жетфунктиондеск

Возвращает описание функции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфунктион* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер функции. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***

Возвращает описание функции. См. [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).

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

 

 




