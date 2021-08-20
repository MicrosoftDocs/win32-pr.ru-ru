---
description: 'ID3DXMATRIXStack: метод:P тельную (D3DX10. h) — добавляет матрицу в стек.'
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: 'ID3DXMATRIXStack: метод:P тельную (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8c9054274666b41e70fa060d10a28309be929a19ee5c363ff4afeb76b25e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914240"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a>ID3DXMATRIXStack: метод:P тельную (D3DX10. h)

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
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




