---
description: Удаляет данные вращения в указанном опорном кадре.
ms.assetid: 8e95d684-fa22-4eba-a721-e7551e8f393b
title: 'Метод ID3DXKeyframedAnimationSet:: Унрегистерротатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 420a15d0086f94def7db8c7d558640d03b69562f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713939"
---
# <a name="id3dxkeyframedanimationsetunregisterrotationkey-method"></a>Метод ID3DXKeyframedAnimationSet:: Унрегистерротатионкэй

Удаляет данные вращения в указанном опорном кадре.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnregisterRotationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор анимации.

</dd> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ключевой кадр.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод работает достаточно долго и не должен использоваться после начала воспроизведения анимации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
