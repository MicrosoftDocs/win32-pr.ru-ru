---
description: Возвращает описание этапа.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Метод ID3DXBaseEffect:: Жетпассдеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713992"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>Метод ID3DXBaseEffect:: Жетпассдеск

Возвращает описание этапа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпасс* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Передача маркера. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

Возвращает описание указанного прохода. См. [**D3DXPASS \_ DESC**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), этот метод возвращает в функции шейдера указатели **null** (в [**D3DXPASS \_ DESC**](d3dxpass-desc.md)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




