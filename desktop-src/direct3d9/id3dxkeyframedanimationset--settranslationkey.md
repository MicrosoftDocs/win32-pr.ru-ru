---
description: Задание сведений о переводе для определенного ключевого кадра в наборе анимации.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'Метод ID3DXKeyframedAnimationSet:: Сеттранслатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713940"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a>Метод ID3DXKeyframedAnimationSet:: Сеттранслатионкэй

Задание сведений о переводе для определенного ключевого кадра в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс анимации.

</dd> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ключевой кадр.

</dd> <dt>

*птранслатионкэй* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Указатель на данные перевода. См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

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

 

 
