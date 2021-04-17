---
description: Возвращает сведения о конкретном обратном вызове в наборе анимации.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703983"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэй

Возвращает сведения о конкретном обратном вызове в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс анимации.

</dd> <dt>

*пкаллбакккэйс* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**

Указатель на [**функцию обратного вызова**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
