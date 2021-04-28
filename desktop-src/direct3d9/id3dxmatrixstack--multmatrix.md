---
description: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3dx9math. h) — определяет продукт текущей матрицы и заданную матрицу.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7361223e8fbcbae0f81641718b216c5903ff6319
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093532"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Мултматрикс (D3dx9math. h)

Определяет произведение текущей матрицы и заданную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмат* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которую необходимо умножить на текущую матрицу.

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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Мултматрикслокал**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




