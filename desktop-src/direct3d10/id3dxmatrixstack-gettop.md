---
description: 'Метод ID3DXMATRIXStack:: GetTop (D3DX10. h) — получает текущую матрицу в верхней части стека.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Метод ID3DXMATRIXStack:: GetTop (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108042"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: GetTop (D3DX10. h)

Извлекает текущую матрицу в верхней части стека.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Этот метод возвращает указатель на структуру D3DXMATRIX, представляющую текущую матрицу.

## <a name="remarks"></a>Remarks

Указатель D3DXMATRIX, возвращаемый этим методом, не обязательно должен быть допустимым после последующих операций с стеком.

Обратите внимание, что этот метод не удаляет текущую матрицу из верхней части стека; Вместо этого он просто возвращает текущую матрицу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
