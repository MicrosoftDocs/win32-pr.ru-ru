---
description: Извлекает текущую матрицу в верхней части стека.
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704011"
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

## <a name="remarks"></a>Комментарии

Указатель D3DXMATRIX, возвращаемый этим методом, не обязательно должен быть допустимым после последующих операций с стеком.

Обратите внимание, что этот метод не удаляет текущую матрицу из верхней части стека; Вместо этого он просто возвращает текущую матрицу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
