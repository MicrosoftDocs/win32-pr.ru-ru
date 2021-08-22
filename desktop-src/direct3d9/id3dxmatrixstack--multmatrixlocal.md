---
description: 'Метод ID3DXMATRIXStack:: Мултматрикслокал (D3dx9math. h) — определяет продукт данной матрицы и текущую матрицу.'
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'Метод ID3DXMATRIXStack:: Мултматрикслокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08a50f6477be6106ce6eaf82c0111f805ed00472259283429e1f638579c91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120818"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Мултматрикслокал (D3dx9math. h)

Определяет произведение заданной матрицы и текущей матрицы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MultMatrixLocal(
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

Этот метод Left — Умножает заданную матрицу на текущую матрицу (преобразование относится к локальному источнику объекта).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт заданной матрицы и текущую матрицу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Мултматрикс**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




