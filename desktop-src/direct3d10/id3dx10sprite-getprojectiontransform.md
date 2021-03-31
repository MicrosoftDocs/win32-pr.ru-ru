---
description: Получите матрицу проекции спрайта, которая применяется ко всем спрайтам.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'Метод ID3DX10Sprite:: Жетпрожектионтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821532"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>Метод ID3DX10Sprite:: Жетпрожектионтрансформ

Получите матрицу проекции спрайта, которая применяется ко всем спрайтам.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппрожектионтрансформ* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) , для которого будет задана матрица проекции спрайта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
