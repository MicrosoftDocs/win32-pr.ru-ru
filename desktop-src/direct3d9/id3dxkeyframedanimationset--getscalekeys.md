---
description: Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'Метод ID3DXKeyframedAnimationSet:: Жетскалекэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713949"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>Метод ID3DXKeyframedAnimationSet:: Жетскалекэйс

Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Анимация* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс анимации.

</dd> <dt>

*пскалекэйс* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Указатель на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод должен заполнять данными шкалы анимации.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: Жетнумскалекэйс**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
