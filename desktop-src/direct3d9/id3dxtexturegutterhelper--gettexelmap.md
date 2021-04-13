---
description: Извлекает координаты текстуры (u, v) каждого шаг текселя.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'Метод ID3DXTextureGutterHelper:: Жеттекселмап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355000"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>Метод ID3DXTextureGutterHelper:: Жеттекселмап

Извлекает координаты текстуры (u, v) каждого шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекселдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на расположение в координатах текстуры (u, v), где размещается каждая шаг текселя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

Для [**классов 2 и 4 пикселей текстуры**](id3dxtexturegutterhelper.md)возвращенные координаты текстуры (u, v) соответствуют ближайшей точке ближайшего треугольника.

Приложение должно выделить Птекселдата и управлять им.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




