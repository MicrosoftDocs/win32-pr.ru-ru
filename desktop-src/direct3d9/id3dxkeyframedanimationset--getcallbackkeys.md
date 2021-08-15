---
description: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс — заполняет массив данными ключа обратного вызова, используемыми для анимации ключевых кадров.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee5a86fa5f016bd6707ec4464c79b1dc182e1ebebde80fa9f73d62e3bba3a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294990"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс

Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкаллбакккэйс* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**

Указатель на выделенный пользователем массив структур [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , который метод должен заполнить данными обратного вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумкаллбакккэйс**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




