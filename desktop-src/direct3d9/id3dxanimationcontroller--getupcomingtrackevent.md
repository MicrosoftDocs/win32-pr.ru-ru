---
description: Возвращает обработчик события для следующего события, запланированного на выполнение после указанного события в дорожке анимации.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Метод ID3DXAnimationController:: Жетупкомингтраккевент (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000318"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Метод ID3DXAnimationController:: Жетупкомингтраккевент

Возвращает обработчик события для следующего события, запланированного на выполнение после указанного события в дорожке анимации.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор трассировки.

</dd> <dt>

*Хевент* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик событий для указанного события, после которого будет осуществляться поиск следующего события. Если задано **значение NULL**, метод вернет следующее запланированное событие.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события для следующего события, запланированного для выполнения в указанной дорожке. Если новое событие не запланировано, возвращается **значение NULL** .

## <a name="remarks"></a>Комментарии

Этот метод можно использовать итеративно для нахождения нужного события путем многократной передачи **значения NULL** для Хевент.

> [!Note]  
> Не переполняйте дальнейшие действия после того, как метод возвращал **значение NULL**.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
