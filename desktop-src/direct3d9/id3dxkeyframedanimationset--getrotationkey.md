---
description: Получение сведений о повороте для определенного ключевого кадра в наборе анимации.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'Метод ID3DXKeyframedAnimationSet:: Жетротатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821437"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a>Метод ID3DXKeyframedAnimationSet:: Жетротатионкэй

Получение сведений о повороте для определенного ключевого кадра в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
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

*протатионкэйс* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md)**

Указатель на данные вращения. См. [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md).

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

 

 
