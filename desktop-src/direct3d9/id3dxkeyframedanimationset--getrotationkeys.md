---
description: Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Метод ID3DXKeyframedAnimationSet:: Жетротатионкэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b95d2591c8eef4b3df22cd8af301bfee9862dd2e3124ecd1cda8d92a589f91df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493543"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a>Метод ID3DXKeyframedAnimationSet:: Жетротатионкэйс

Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
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

*протатионкэйс* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md)**

Указатель на выделенный пользователем массив [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md) кватернион, который метод заполнит заливкой данными вращения анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумротатионкэйс**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
