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
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713855"
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
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
