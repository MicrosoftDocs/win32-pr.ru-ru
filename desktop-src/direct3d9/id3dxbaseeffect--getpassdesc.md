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
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987754"
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

## <a name="remarks"></a>Remarks

> [!Note]  
> Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), этот метод возвращает в функции шейдера указатели **null** (в [**D3DXPASS \_ DESC**](d3dxpass-desc.md)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




