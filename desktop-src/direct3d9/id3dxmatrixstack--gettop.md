---
description: 'Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h) — получает текущую матрицу в верхней части стека.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093582"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h)

Извлекает текущую матрицу в верхней части стека.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Этот метод возвращает указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую текущую матрицу.

## <a name="remarks"></a>Remarks

Указатель [**D3DXMATRIX**](d3dxmatrix.md) , возвращаемый этим методом, не обязательно должен быть допустимым после последующих операций с стеком.

Обратите внимание, что этот метод не удаляет текущую матрицу из верхней части стека; Вместо этого он просто возвращает текущую матрицу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P Op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P тельную**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




