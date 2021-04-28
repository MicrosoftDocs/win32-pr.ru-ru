---
description: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h) — определяет продукт текущей матрицы и заданную матрицу.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107972"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h)

Определяет произведение текущей матрицы и заданную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на структуру D3DXMATRIX, которую необходимо умножить на текущую матрицу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод дает право на умножение заданной матрицы в текущую матрицу (преобразование относится к текущему источнику мира).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт текущей матрицы и заданную матрицу.

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

 

 
