---
description: Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'Метод ID3DXKeyframedAnimationSet:: Жетскалекэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 199b5596e05bd013f3384c2a182bbe8e905cb609ae869c194d811fb97d3d254b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121161"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a>Метод ID3DXKeyframedAnimationSet:: Жетскалекэй

Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
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

*Ключ* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ключевой кадр.

</dd> <dt>

*пскалекэйс* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Указатель на данные шкалы. См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

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
</dt> </dl>

 

 
