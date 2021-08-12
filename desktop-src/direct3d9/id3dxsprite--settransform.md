---
description: Задает преобразование спрайта.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'Метод ID3DXSprite:: Сеттрансформ (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fba7c21d0ba0e99aefc5c4d5dfd69301bb706f804e736badcbe0227d58aca81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292621"
---
# <a name="id3dxspritesettransform-method"></a>Метод ID3DXSprite:: Сеттрансформ

Задает преобразование спрайта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птрансформ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий преобразование спрайта из исходного мира. Используйте это преобразование для масштабирования, вращения или преобразования спрайта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[Преобразования (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




