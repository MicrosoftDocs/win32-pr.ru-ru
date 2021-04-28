---
description: 'ID3DXMATRIXStack: метод:P тельную (D3dx9math. h) — добавляет матрицу в стек.'
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: 'ID3DXMATRIXStack: метод:P тельную (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093511"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a>ID3DXMATRIXStack: метод:P тельную (D3dx9math. h)

Добавляет матрицу в стек.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Push();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод увеличивает число элементов в стеке на 1, повторяя текущую матрицу. Стек будет увеличиваться динамически по мере добавления элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P Op**](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




