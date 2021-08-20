---
description: Возвращает обработчик событий для события, которое в данный момент выполняется в указанной дорожке анимации.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Метод ID3DXAnimationController:: Жеткурренттраккевент (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d61902765c29808941637d4ce7ebb7f4b361ac6904abc1fae5907738162347a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094515"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>Метод ID3DXAnimationController:: Жеткурренттраккевент

Возвращает обработчик событий для события, которое в данный момент выполняется в указанной дорожке анимации.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор трассировки.

</dd> <dt>

*Тип события* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXEVENT \_ тип**](./d3dxevent-type.md)**

Тип события для запроса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик событий для события, выполняемого в данный момент в указанной дорожке. Если в указанной дорожке не запущена ни одно событие, возвращается **значение NULL** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
