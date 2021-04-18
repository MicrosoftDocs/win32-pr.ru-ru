---
description: Применяет набор анимации к указанной дорожке.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Метод ID3DXAnimationController:: Сеттракканиматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713889"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>Метод ID3DXAnimationController:: Сеттракканиматионсет

Применяет набор анимации к указанной дорожке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор курса, к которому применяется набор анимации.

</dd> <dt>

*панимсет* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Указатель на набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) , который должен быть добавлен к дорожке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Этот метод задает для набора анимации заданную запись для смешения. Набор анимации для каждой записи смешивается в соответствии с толщиной и скоростью записи при вызове [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
