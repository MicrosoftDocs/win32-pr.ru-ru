---
description: Возвращает обработчик события для следующего приоритетного события Blend, которое было запланировано после указанного события.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Метод ID3DXAnimationController:: Жетупкомингприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424322"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>Метод ID3DXAnimationController:: Жетупкомингприоритибленд

Возвращает обработчик события для следующего приоритетного события Blend, которое было запланировано после указанного события.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Хевент* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик событий для указанного события, после которого будет осуществляться поиск следующего события с приоритетом Blend. Если задано **значение NULL**, метод вернет следующее запланированное событие смешения приоритета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события для следующего запланированного события смешения приоритета. Если не запланировано новое событие смешения приоритета, возвращается **значение NULL** .

## <a name="remarks"></a>Комментарии

Этот метод можно использовать итеративно для нахождения требуемого события смешения приоритета путем многократной передачи **значения NULL** для Хевент.

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

 

 




